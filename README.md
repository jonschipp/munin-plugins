munin-plugins
=============

Munin Plug-ins

### Rsyslog
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

### OSSEC

Plugins to graph OSSEC stats for Munin

* munin/ossec_ar_stats - Graph active response script usage
* munin/ossec_stats - Graph alert counts by 3 major types of alerts: rules, syscheck, or rootcheck
* munin/ossec_top_groups - Graph alert counts by top 10 rule categories
* munin/ossec_top_rules - Graph alert counts by top 10 rule descriptions

Location
```
$ ls /etc/munin/plugins/ossec_*
/etc/munin/plugins/ossec_ar_stats /etc/munin/plugins/ossec_stats  /etc/munin/plugins/ossec_top_groups /etc/munin/plugins/ossec_top_rules
```

Configuration
```
$ cat /etc/munin/plugin-conf.d/ossec_*
[ossec_ar_stats]
user root
[ossec_stats]
user root
[ossec_top_groups]
user root
[ossec_top_rules]
user root
```

![OSSEC](https://raw.githubusercontent.com/ncsa/ossec-tools/master/munin/ossec_munin.png)
