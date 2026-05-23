# 4.Execution_of_NetworkCommands
## AIM :Use of Network commands in Real Time environment
## Software : Command Prompt And Network Protocol Analyzer
## Procedure: To do this EXPERIMENT- follows these steps:
<BR>
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer 
<BR>
All commands related to Network configuration which includes how to switch to privilege mode
<BR>
and normal mode and how to configure router interface and how to save this configuration to
<BR>
flash memory or permanent memory.
<BR>
This commands includes
<BR>
• Configuring the Router commands
<BR>
• General Commands to configure network
<BR>
• Privileged Mode commands of a router 
<BR>
• Router Processes & Statistics
<BR>
• IP Commands
<BR>
• Other IP Commands e.g. show ip route etc.
<BR>

## Program
CLIENT
```
client.py
import socket
from pythonping import ping
s=socket.socket() s.bind(('localhost'8000)) s.listen(5) c,addr=s.accept()
while True: hostname=c.recv(1024).decode() try:
c.send(str(ping(hostname, verbose=False)).encode())
except KeyError:
c.send("Not Found".encode())
```
SERVER
```
server.py

import socket s=socket.socket() s.connect(('localhost',8000)) while True:
ip=input("Enter the website you want to ping ")
s.send(ip.encode())
print(s.recv(1024).decode())
```
## Output

## NETSTAT

<img width="1917" height="903" alt="image" src="https://github.com/user-attachments/assets/225befc9-5584-44b0-b964-33b1ec6b06e5" />

## IP CONFIGURATION

<img width="1898" height="899" alt="image" src="https://github.com/user-attachments/assets/edf719d2-2038-4f2c-bd9f-9c79b79af802" />

## GETMAC

<img width="1781" height="370" alt="image" src="https://github.com/user-attachments/assets/6939788b-44a6-4dad-8c6b-5e480b979330" />

## ARP

<img width="1859" height="900" alt="image" src="https://github.com/user-attachments/assets/d52b4884-bd84-4f8b-af98-0007666d22d8" />

## SYSTEM INFO

<img width="1892" height="904" alt="image" src="https://github.com/user-attachments/assets/181f00d7-03c0-4a0c-96bf-537467009db7" />

## NBTSTAT

<img width="1706" height="851" alt="image" src="https://github.com/user-attachments/assets/ac1bd578-116b-4386-b1c9-9674c4d0ea00" />

## HOSTNAME

<img width="971" height="341" alt="image" src="https://github.com/user-attachments/assets/92930384-3d63-490e-bd33-ab3dc9de17a7" />

## NS LOOKUP

<img width="558" height="123" alt="image" src="https://github.com/user-attachments/assets/a99a746b-76ae-45bd-aee7-cebcbefb91c8" />

## PING

<img width="1050" height="753" alt="image" src="https://github.com/user-attachments/assets/1ce1ccc9-1d16-4389-aa96-ef9caf08075a" />

## TRACET

<img width="1004" height="139" alt="image" src="https://github.com/user-attachments/assets/45e7678b-c20f-465d-831b-79fec12e5eb0" />

## Result
Thus Execution of Network commands Performed 
