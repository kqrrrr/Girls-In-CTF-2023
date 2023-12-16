# Frequency (Points: 100)

## Problem
> I can hear flag...I think....or I am insane?
* [changelle.wav](https://scoreboard.girls4ctf.online/files/7db412504a9c2c7e3c5ad5583f7ce682/challenge.wav?token=eyJ1c2VyX2lkIjoxNiwidGVhbV9pZCI6MjQsImZpbGVfaWQiOjQ2fQ.ZX1HZQ.SCO2piLSp-D-7YwlbVii1wRACUk)

## Solution
We need to get the flag from the given audio file.
```console
sox challenge.wav -n spectrogram -o challenge.png
```
Open challenge.png, you will see the flag:
* [challenge.png]()

## Flag
> GCTF2023{this_fl4g_sounds_weirddddddd}
