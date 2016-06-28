===========================================
Conversion Tracking
===========================================


Automatically capturing form submissions
===========================================
You can automatically track all form submissions on your site.

Choose the automatically capture checkbox from https://app.ruleranalytics.com/#/site_settings


Manually capturing your data
===========================================

HTML forms with POST action
---------------------------
For standard (old school) HTML forms add a conversion javascript tag to your ``checkout`` or ``thank you`` page

.. code-block:: html
    :linenos:

    <script type="text/javascript">

        var RulerAnalyticsPayload = {
          action: 'convert', // you can use any goal name here like sale, contact or 'add to basket'
          variable: 'PopulateWithVariable', // any additional variables can be added in here


          order_id: '<?php echo $orderId; ?>' // Add a server side variable using PHP
        };

    </script>


this needs to appear above the :doc:`tracking javascript tag <tag>` tag. The ``<head>`` tag is a good place to start.


Wordpress Capture Form 7
---------------------------

This plugin for wordpress submits the forms via ``ajax``. To capture data from the form we need to configure the *****
post settings.

.. code-block:: javascript

    on_sent_ok: 'var email=RulerAnalytics.__sz("input[name=your-email]")[0].value;RulerAnalytics.RegisterAction({ uid: "56d04f7c8c0d4", action:"convert", email:email});’


Or from version 1.1 of ruler analytics

.. code-block:: javascript

    RulerAnalytics.trackForm('input', 'formselector', 'goalname')

