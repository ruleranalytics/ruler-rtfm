========================
Phone Call Tracking
========================

.. Important::
    This is a work in progress... please don't use anything yet

Please `contact us <http://www.ruleranalytics.com/contact>`_ to request changes to your account to include Phone Call tracking.

Google Analytics Integration
==============================

Ruler Analytics provides a zero-configuration approach to integrating phone calls with Google Analytics. Enable this feature from
the `site settings <https://app.ruleranalytics.com/#/site-settings>`_ or `call settings <https://app.ruleranalytics.com/#/setup-call-tracking>`_ pages.

Configuring your Google Analytics Site
---------------------------------------

To receive events from Ruler Analytics you must configure GA as follows.

1. Create a goal
2. Configure the goal to monitor ruler analytics inbound call events
3. Save


Testing your GA integration
----------------------------

Either contact us and we can run a test manually or (if you don't mind getting technical) use the hitbuilder with the parameters below.

https://ga-dev-tools.appspot.com/hit-builder/

Hit builder parameters::

    v=1&t=event&tid=UA-XXXYYYZZ-1&cid=e054966c-f9e2-4273-9179-18d4855af092&ec=TestCall&ea=TestInbound&el=TestNumber


Don't forget to replace the ``UA-XXXYYYYZZ-1`` tracking id with your own Google Analytics tracking Id :)


