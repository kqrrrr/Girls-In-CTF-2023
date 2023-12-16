# Wireshark #2 (Points: 400)
## Problem 
> I remember there is a compressed file. Please find it and expose the secret!
Same challenge file as Wireshark #1

> Hint: If you found the file, it may require further CPR

* [challenge.pcap](https://scoreboard.girls4ctf.online/files/820316b9dde67ff8ef6aaffd76e1450e/challenge.pcap?token=eyJ1c2VyX2lkIjoxNiwidGVhbV9pZCI6MjQsImZpbGVfaWQiOjQ4fQ.ZX1e3g.Zs-DW4xoawNrhx2hh_jq2yvT89g)

## Solution
From the description, we know that there is a compressed file in the packet. 
Filter the packet to "html", you will saw a secret.zip file.
So, to get the secret.zip file, you need to go to File > Export Objects > HTTP > Choose secret.zip file and Save it.

But when you try to unzip the file, it show some errors.
![image](https://github.com/kqrrrr/Girls-In-CTF-2023/assets/95967644/e114aaff-e2e5-4375-906c-539cf7639c99)
So I try to use 7-zip to extract the files. But it asked me to enter the password, so I use rockyou.txt to crack the password. 
```console
fcrackzip -D -p rockyou.txt -v -u secret.zip
```

Finally, we know the password is "batman". Then open the flag.txt file inside to get the flag.

## Flag
> GCTF2023{C0rrupted_Z1p_f1l3s}
