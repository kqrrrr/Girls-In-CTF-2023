# Broken (Points: 100) (Difficulty: Easy)

## Problem
> I got this pdf and it's very important to me. WHY CAN'T IT OPEN OMG!

> [Challenge.pdf](https://github.com/kqrrrr/Girls-In-CTF-2023/files/13692213/Challenge.pdf)


## Solution

The PDF document is damaged.

![image](https://github.com/kqrrrr/Girls-In-CTF-2023/assets/96009671/729fe304-f421-47cf-811b-de0f93e9499e)


In Kali Linux Terminal, type the following commands:


> sudo apt-get install mupdf-tools


![image](https://github.com/kqrrrr/Girls-In-CTF-2023/assets/96009671/5a2c181f-687d-453a-92e4-6a3eeabab8fe)


Then, change your directory to where you stored the PDF document. In this case, I stored the PDF document at Desktop.

![image](https://github.com/kqrrrr/Girls-In-CTF-2023/assets/96009671/7dd63e6c-113b-410f-9673-8d3fdfddc486)


Type the following commands:

> mutool clean Challenge.pdf Repaired_Challenge.pdf


![image](https://github.com/kqrrrr/Girls-In-CTF-2023/assets/96009671/013f310f-161a-49c8-8a2b-533be0c95d27)

Here is the Repaired_Challenge PDF document!

![image](https://github.com/kqrrrr/Girls-In-CTF-2023/assets/96009671/315f2a76-f1e5-4164-8d7b-426f0f4bb38b)

![image](https://github.com/kqrrrr/Girls-In-CTF-2023/assets/96009671/8d148225-f224-4d4a-8068-c062d764b463)

![image](https://github.com/kqrrrr/Girls-In-CTF-2023/assets/96009671/7e54d648-9c70-4e83-8b91-40e20cc02a2e)

At the bottom of the last page, we found the Flag !!!

## Flag

![image](https://github.com/kqrrrr/Girls-In-CTF-2023/assets/96009671/dfa53a78-fa92-4465-bf37-d5e1ce445966)




