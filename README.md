# Networking_cmds

To successfully understand the basic networking concepts.



Networking Command

These commands are as follow-

1. Ping

Ping is used to testing a network host capacity to interact with another host. Just enter the command Ping, followed by the target host’s name or IP address. The ping utilities seem to be the most common network tool. This is performed by using ICMP, which allows the echo packet to be sent to the destination host and a listening mechanism. If the destination host reply to the requesting host, that means the host is reachable. This utility usually gives a basic image of where there may be a specific networking issue,

For Example: If an Internet connection is not in the office, for instance, the ping utility is used to determine if the problem exists in the office or the Internet provider’s network. The following shows an image of how ping tools to obtain the locally connected router’s connectivity status.

There are various options a user can use with the Ping command.

Options with Description

<br>A. target: This is the destination IP address or a hostname user want to ping.
<br>B. -a: This option resolves the hostname of an IP address target.
<br>C. -t: This ping command option will ping the target until you stop it by pressing Ctrl-C.
<br>D. -n count: This option is used to set the number of ICMP Echo Requests to send, from 1 to 4294967295. If -n is not specified, the ping command will return 4 by default.
<br>E. -l size: This option is used to set the size, in bytes, of the echo-request packet from 32 to 65,527. If the -l option is not specified, the ping command will send a 32-byte echo request.
<br>F. -s count: This option is used to report the time in the Internet Timestamp format that each echo request is received and an echo reply is sent. The maximum count value is 4, i.e. only the first four hops can be time stamped.
<br>G. -r count: This command uses the ping command option to specify the number of hops between the source computer and the target computer. The maximum count value is 9; the Tracert command can also be used if the user wants to view all the hops between two devices.
<br>H. -i TTL: This ping command option sets the Time to Live (TTL) value; the maximum value is 255.
<br>I. -f: Use this ping command option to prevent ICMP Echo Requests from being fragmented by routers between the source and the target. The -f option is often used to troubleshoot Path Maximum Transmission Unit (PMTU) issues.
<br>J. -w timeout: A timeout value must be specified while executing this ping command. It adjusts the amount of time in milliseconds. If the -w option is not specified, then the default timeout value of 4000 is set, which is 4 seconds.
<br>K. -p: To ping a Hyper-V Network Virtualization provider address.
<br>L. -S srcaddr: This option is used to specify the source address.

2. NetStat

Netstat is a Common TCP – IP networking command-line method present in most Windows, Linux, UNIX, and other operating systems. The netstat provides the statistics and information in the use of the current TCP-IP Connection network about the protocol.

There are various options a user can use with the Netstat command.


<br>i. -a: This will display all connection and ports
<br>ii -b: Shows the executable involved in each connection or hearing port
<br>iii. -e: This protocol will combine with the -sand display the ethernet statistics
<br>iv. -n: This will display the address and the port number in the form of numerical
<br>v. -o: It will display the ID of each connection for the ownership process.
<br>vi. -r: It will display the routing table
<br>vii. -v: When used in combination with -b, the link or hearing port sequence for every executable is shown.

3. Ip Config

The command IP config will display basic details about the device’s IP address configuration. Just type IP config in the Windows prompt and the IP, subnet mask and default gateway that the current device will be presented. If you have to see full information, then type on command prompt config-all and then you will see full information. There are also choices to assist you in resolving DNS and DHCP issues.

4. Hostname

To communicate with each and other, the computer needs a unique address. A hostname can be alphabetic or alphanumeric and contain specific symbols used specifically to define a specific node or device in the network. For example, a hostname should have a domain name (TLD) of the top-level and a distance between one and 63 characters when used in a domain name system (DNS) or on the Internet.

Steps to Determine Your Computer’s Name
<br>Open a terminal window and type the command given below.
<br>
<br>i. hostname
It will provide the name of your computer. The first part of the result is the name of a computer and the second part is the name of the domain.
To get only the computer name, run the following command:
<br>ii. hostname -s
The output will be localhost.
Similarly, if a user wants to find out which domain system is running, then use the following command.
<br>iii. hostname -d
The IP address for the hostname can also be retrieved by using the following command.”
<br>iv. hostname -i
User can find out all the aliases for the computer by using the command given below.
<br>v. hostname -a

5. Tracert

The tracert command is a command which is used to get the network packet being sent and received and the number of hops required for that packet to reach to target. This command can also be referred to as a traceroute. It provides several details about the path that a packet takes from the source to the specified destination.

The tracert command is available for the Command Prompt in all Windows operating systems.

The syntax for Tracert Command

tracert [-d] [-h MaxHops] [-w TimeOut] target

There are various options the user can use with tracert command.

Options for tracert Command are as follows-

<br>i. target: This is the destination, either an IP address or hostname.
<br>ii. –d: This option prevents Tracert from resolving IP addresses to hostnames to get faster results.
<br>iii. -h MaxHops: This Tracert option specifies the maximum number of hops in the search for the target. If the MaxHops option is not specified the target has not been found by 30 hops, then the tracert command will stop looking.
<br>iv. -w timeout: A timeout value must be specified while executing this ping command. It adjusts the amount of time in milliseconds.
<br>
6. Nslookup

The Nslookup, which stands for name server lookup command, is a network utility command used to obtain information about internet servers. It provides name server information for the DNS (Domain Name System), i.e. the default DNS server’s name and IP Address.

The syntax for Nslookup is as follows.

Nslookup

or

Nslookup [domain_name]

7. Route

In IP networks, routing tables are used to direct packets from one subnet to another. The Route command provides the device’s routing tables. To get this result, just type route print. The Route command returns the routing table, and the user can make changes by Commands such as Route Add, Route Delete, and Route Change, which allows modifying the routing table as a requirement.

8. ARP

Although network communications can readily be thought of as an IP address, the packet delivery depends ultimately on the media access control (MAC). This is where the protocol for address resolution comes into effect. You can add the remote host IP address, which is an arp -a command, in case you have issues to communicate with a given host. The ARP command provides information like Address, Flags, Mask, IFace, Hardware Type, Hardware Address, etc.

9. Path Ping

We discussed the Ping command and the Tracert command. There are similarities between these commands. The pathping command which provides a combination of the best aspects of Tracert and Ping.

This command takes 300 seconds to gather statistics and then returns reports on latency and packet loss statistics at intermediate hops between the source and the target in more detail than those reports provided by Ping or Tracert commands.

The syntax for path ping is as follows:

path ping [-n] [-h] [-g <Hostlist>] [-p <Period>] [-q <NumQueries> [-w <timeout>] [-i <IPaddress>] [-4 <IPv4>] [-6 <IPv6>][<TargetName>]

<br>i. N: Prevents path ping functioning from attempting to resolve routers’ IP addresses to their names.
<br>ii. -h MaxHops: This tracert option specifies the maximum number of hops in the search for the target. If the MaxHops option is not specified the target has not been found by 30 hops then the tracert command will stop looking.
<br>iii. -w timeout: A timeout value must be specified while executing this ping command. It adjusts the amount of time in milliseconds.
<br>iv. -ip <IPaddress>: Indicates the source address.
<br>v. target: This is the destination IP address or a hostname user want to ping.
