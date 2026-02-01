# zabbix-template-librehardwaremonitor
A Zabbix Template to get sensor information from LibreHardwareMonintor via WebServer.

## Installation

 - Install Libre Hardware Monitor on machine
 - Enable webserver inside of LibreHardwareMonitor and configure according firewall rule
 - Set Libre Hardware Monitor to `Run on Windows startup` or configure it as windows service (with something like [Servy](https://github.com/aelassas/servy))
 - Import the template in `/template` to your Zabbix Server instance, and assign it to a host and configure `{$LHWM_URL}` macro on host

## Stuff

 - You don't really need a zabbix agent on endpoint, since template is configure to directly access web server of LHWM
 - I've tested this running running LHWM version 0.9.5.0
 - Since some version of LHWM there is no WMI exporter, hence rewrite to use HTTP web server
 - JS parts of template written with help of LLM.
 - The template doesn't have any triggers in it, it was done mostry to gather historical data on my personal PC. If you want to create triggers, your probably should go with LLD overrides (well, I would go that way)
 - Template was created on Zabbix 6.0 LTS, but probably would be easily portable up to 5.0
