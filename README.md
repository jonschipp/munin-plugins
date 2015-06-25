munin-plugins
=============

Munin Plug-ins

The names of the rsyslog queues must be listed in the following files for the rsyslog plugins to work.
The plugins will only display output for the listed queues.
```
$ ls -1 /etc/munin/plugin-conf.d/rsyslog_*
/etc/munin/plugin-conf.d/rsyslog_discarded.conf
/etc/munin/plugin-conf.d/rsyslog_messages.conf
/etc/munin/plugin-conf.d/rsyslog_queued.conf

$ cat /etc/munin/plugin-conf.d/rsyslog_*
[rsyslog_discarded]
env.QUEUES
main:analysis-sec:analysis-sec\[DA\]:cyclone:cyclone\[DA\]:seclogs:seclogs\[DA\]

[rsyslog_messages]
env.QUEUES
main:analysis-sec:analysis-sec\[DA\]:cyclone:cyclone\[DA\]:seclogs:seclogs\[DA\]

[rsyslog_queued]
env.QUEUES
main:analysis-sec:analysis-sec\[DA\]:cyclone:cyclone\[DA\]:seclogs:seclogs\[DA\]
```

Examples:
![Number of Messages](http://sickbits.net/wordpress/wp-content/uploads/2014/08/Screen-Shot-2014-08-06-at-5.54.02-PM.png)
![Number of Queued Messages](http://sickbits.net/wordpress/wp-content/uploads/2014/08/Screen-Shot-2014-08-06-at-5.54.12-PM.png)
