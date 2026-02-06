# zabbix-template-librehardwaremonitor
A Zabbix Template to get sensor information from LibreHardwareMonintor via WMI.

## Installation

 - Install Libre Hardware Monitor on machine (and zabbix agent if it is not)
 - Set Libre Hardware Monitor to `Run on Windows startup` or configure it as windows service (with something like [Servy](https://github.com/aelassas/servy))
 - Import the template `Template Application - LibreHardwareMonitor WMI.yaml` in `/template` to your Zabbix Server instance, and assign it to a host.

## Stuff

 - I've tested this running running LHWM version 0.9.4. 0.9.5 doesn't have WMI in it (you can use old template, which utilizes web-server, but use it on your own risk)
 - The template doesn't have any triggers in it, it was done mostry to gather historical data on my personal PC.
 - Template was created on Zabbix 6.0 LTS, but probably would be easily portable up to 5.0
