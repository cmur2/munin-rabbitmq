=========================
 RabbitMQ Munin Plug-Ins
=========================

Installation
============

Copy the plug-ins to the munin plugin directory, e.g ``/etc/munin/plugins/``.

Granting Permissions
====================

To use these plug-ins you have to tell munin-node to execute them as
root by changing the plug-in configuration file (on debian that is
``/etc/munin/plugin-conf.d``)::

    [rabbitmq_connections]
    user root

    [rabbitmq_queue_consumers]
    user root

    [rabbitmq_queue_disk]
    user root

    [rabbitmq_queue_memory]
    user root

    [rabbitmq_queue_messages]
    user root


Using a Custom Virtual Host
============================

You can set the name of virtual host by changing the plug-in configuration
file (on debian that is ``/etc/munin/plugin-conf.d``)::

    [rabbitmq_queue_consumers]
    env.vhost vhostname

    [rabbitmq_queue_disk]
    env.vhost vhostname

    [rabbitmq_queue_memory]
    env.vhost vhostname

    [rabbitmq_queue_messages]
    env.vhost vhostname
