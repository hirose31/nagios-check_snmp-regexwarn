nagios-check_snmp-regexwarn
===============

This is extended check_snmp plugin to return WARNING state if regular
expression matches.

usage
---------------

provides -g (-G) option just like -r (-R) option.

example:

    check_command  check_snmp -P 1 -C public -H $HOSTADDRESS$ -o extOutput.1 -r OK -g VERYFY

return OK state if output string of extOutput.1 matches "OK".
return WARNING state if output matches "VERIFY".
return CRITICAL state if output does not match neither "OK" nor "VERIRY".

