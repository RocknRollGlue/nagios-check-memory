# nagios plugin check-memory
Compatible with Icinga2 and Graphite
In order to fully load this plugin, the following requirements has to be met, both from standard APT packages:
python3-pip
python3

## Setup
Place the check_memory.py in the plugins folder on the Icinga2 agent. Default folder is /usr/lib/nagios/plugins
In Icinga2 director, add a new command, with the "Command" field as check_memory.py

Arguments added are all optional but you can add the following arguments:
Argument name: -w
Description: Threshold % of warning levels of memory available. Defaults to 70
Value type: String
Value: \$warning_level\$
Condition format: String
Required: No

Argument name: -c
Description: Threshold % of critical levels of memory available. Defaults to 90
Value type: String
Value: \$critical_level\$
Condition format: String
Required: No


Add the custom fields in the command, or in the service template desired.
