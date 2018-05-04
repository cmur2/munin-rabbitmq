=========================
 RabbitMQ Munin Plug-Ins
=========================

Installation
============

Copy the plug-ins to the munin plugin directory, e.g ``/etc/munin/plugins/``.


Using a Custom Virtual Host
============================

You can set the name of virtual host by changing the plug-in configuration
file (on debian that is ``/etc/munin/plugin-conf.d``)::

    [rabbitmq_connections]
    env.url http://guest:guest@127.0.0.1:15672

    [rabbitmq_queue_consumers]
    env.url http://guest:guest@127.0.0.1:15672

    [rabbitmq_queue_disk]
    env.url http://guest:guest@127.0.0.1:15672

    [rabbitmq_queue_memory]
    env.url http://guest:guest@127.0.0.1:15672

    [rabbitmq_queue_messages]
    env.url http://guest:guest@127.0.0.1:15672
