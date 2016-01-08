
####AppliedFirewall ####
### 2014-09-06 ###

##Definition Files (definitions/)##
Defines IPTable Polices, Ports, Host and Networks
#1. definitions/polices#
	- DEBUG_MODE [YES/NO]		:	Enables or Disables system stderr
	- DEFAULT_INPUT	[ACCEPT/DROP]	:	Default Policy for INPUT CHAIN
	- DEFAULT_OUTPUT [ACCEPT/DROP]	:	Default Policy for OUTPUT CHAIN
	- DEFAULT_FORWARD [ACCEPT/DROP]	:	Default Policy for DEFAULT_FORWARD CHAIN
	- YUM_ENABLE [YES/NO]		:	Yum Repo list HTTP Allowed IPs

#2. definitions/ports#
	- Defines Ports to be used with this AppliedFirewall
	- Variable names (PORT Names) must be suffixed with "PORT_" (without quotes)
	- Example: To define FTP Port, the PORT_FTP="20 21" must exist on this file

##Rule Files##
rules/
  - advanced.forward
  - advanced.in_append
  - advanced.in_prepend
  - advanced.out_append
  - advanced.out_prepend
  - allow.in_icmp
  - allow.in_tcp_from_hosts
  - allow.in_tcp_ports_from_any
  - allow.in_tcp_ports_from_hosts
  - allow.in_udp_from_hosts
  - allow.in_udp_ports_from_any
  - allow.in_udp_ports_from_hosts
  - allow.out_icmp
  - allow.out_tcp_ports_to_any
  - allow.out_tcp_ports_to_hosts
  - allow.out_tcp_to_hosts
  - allow.out_udp_ports_to_any
  - allow.out_udp_ports_to_hosts
  - allow.out_udp_to_hosts
