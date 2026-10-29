# VirtualBox NAT Network Setup for Kali Linux
What you will need, Kali linux, virtualbox

For this lab, I created a custom NAT Network in VirtualBox and assigned a manual IP address to my Kali Linux VM.

First, I opened VirtualBox and went to `Tools > Network > NAT Networks`. I created a new NAT Network called `NatNetwork1` and set the IPv4 prefix to `10.0.0.0/24`. I also disabled DHCP because I wanted to assign the IP address manually.

After that, I opened the Kali VM settings and went to `Network > Adapter 1`. I changed the adapter mode to `NAT Network` and selected `NatNetwork1`.

Once Kali started, I checked the network interfaces with:

ip a

My active interface was `eth0`.

I then removed the current IP address from the interface:

sudo ip addr flush dev eth0


Then I assigned the IP address `10.0.0.2/24`:

sudo ip addr add 10.0.0.2/24 dev eth0


Finally, I checked the configuration again using:

ip a

The Kali VM was now using:

10.0.0.2/24


This setup gives me a simple and predictable network for my cybersecurity lab, where I can manually control the IP addresses of each virtual machine.
Thanks for NETWORKWALKS for the opportunity. 
