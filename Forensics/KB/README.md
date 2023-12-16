# KB (Points: 500) (Difficulty: Hard)
## Problem
> Hmm, haven't seen this type of wireshark file in a while now.
* [challenge.pcapng](https://scoreboard.girls4ctf.online/files/1aadf20d8b34c837fc2b7a7ec5abaeb6/challenge.pcapng?token=eyJ1c2VyX2lkIjoxNiwidGVhbV9pZCI6MjQsImZpbGVfaWQiOjQ5fQ.ZX1jPQ.f628r5vPenql9Kpw2ssv2KNIoPc)

## Solution
Open the wireshark, the packets shown are in usb protocol. Since this is new to me, I tried to google and found this: https://ctf-wiki.mahaloz.re/misc/traffic/protocols/USB/. 
I try to extract the Leftover Capture Data field.
```console
tshark -r challenge.pcapng -T fields -e usb.capdata > usbdata.txt
```
Open usbdata.txt, you can see the size of data is 8 bytes
![image](https://github.com/kqrrrr/Girls-In-CTF-2023/assets/95967644/b4d4ad08-a328-4cc8-8004-b4299932a4cb)

The third byte of each USB packet represents the key code. So I use [usb.py](https://github.com/kqrrrr/Girls-In-CTF-2023/blob/main/Forensics/KB/usb.py) script to extract keystrokes from USB packets captured in pcapng file.
```console
python usb.py challenge.pcapng
```
Try to run the python code with the challenge.pcapng file. Then, get the flag.
![image](https://github.com/kqrrrr/Girls-In-CTF-2023/assets/95967644/bf27f923-ad11-47c1-b604-4a1d0fed72ec)

## Flag
> GCTF2023{1nt3rc3pt1ng_keystr0k3}
