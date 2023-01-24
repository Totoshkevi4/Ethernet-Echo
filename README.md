# Ethernet-Echo
Echo on VHDL with Cyclone II and DM9000A

Warning!
This version is not fully working (at least it wasn't when I was testing last time).

Main goal is to make 'echo' on Ethernet line. Module swaps MAC-adresses of received signal and send it back if it's not an ARP frame.
If DM9000A receives ARP request, then we send it back with our current IP and make it response (changing OPER to 0x0002). 
