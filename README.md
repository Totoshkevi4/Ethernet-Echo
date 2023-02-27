# Ethernet Echo on VHDL
Echo implementation on VHDL with Cyclone II (EP2C35) and DM9000A. 

It was a study project for FPGA class, it was coded with my groupmate. For testing we used [Altera DE2 board](https://www.terasic.com.tw/cgi-bin/page/archive.pl?Language=English&CategoryNo=183&No=30&PartNo=1#contents) (caareful, not the Altera DE2-115 or the other versions).

Schematic and summary on Russian can be found [here](https://disk.yandex.ru/d/-lgtGx38ATc5Hg).

__Warning!__ 
This version of echo is not fully working (at least it wasn't when I was testing last time). It can echo some of the packages.

## How it works

Main goal was to make 'echo' on Ethernet line. Module swaps MAC-adresses of received signal and send it back if it's not an ARP frame.

If DM9000A receives ARP request, then it should send it back with our current IP and make it response (changing OPER field to 0x0002).

Program starts as soon as you power FPGA, there is no reset buttons.
IP adress of DM9000A is displayed on LCD1602.