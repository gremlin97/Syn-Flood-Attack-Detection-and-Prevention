Project Title-Syn Flood Attack Detection and Prevention

Group Members-

Kunal.S.Kasodekar-15bce1045
Kora Sriram Teja-15bce1034
Gourab Singha-15bce1336

IP's of source and destination machines for Syn flood Attack via Hping3-

Source IP-192.168.31.128
Target IP-192.168.31.1
Target Port-135
Host name-sriram@ubuntu(Virtual Machine)
Target Machine-Percy(WIndows Machine)

Commands to generate Traffic

- Type {sudo hping3 -S Ågattackers IPÅh -a Ågvictims IPÅh -p 135 ?flood} in the terminal of the VM.
Here -S sets hping3 in syn packet generation mode, -p sets port used by these packets, --flood set hping3 in flood mode.

-Attack through hping3

Here is an implementation of a syn flood attack in a virtual machine with ipv4 address of 192.168.31.128. this machine Is sending syn packets  to the host machine whose IP is 192.168.31.1.

hping3 -S 192.168.31.128  -a  192.31.1.1 -p 135 --flood
192.168.56.2 is your target IP address. -p 135 denotes the port to be attacked.
You can even spoof the ip address fo the source.If we fill the spoof IP Parameter as IP 192.168.1.1 it is the spoofed IP then the victim will think the traffic is coming from 192.168.1.1.
