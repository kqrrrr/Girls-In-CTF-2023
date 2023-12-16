# Frequency (Points: 100) (Diffulty: Easy)

## Problem
> I can hear flag...I think....or I am insane?
* [changelle.wav](https://scoreboard.girls4ctf.online/files/7db412504a9c2c7e3c5ad5583f7ce682/challenge.wav?token=eyJ1c2VyX2lkIjoxNiwidGVhbV9pZCI6MjQsImZpbGVfaWQiOjQ2fQ.ZX1HZQ.SCO2piLSp-D-7YwlbVii1wRACUk)

## Solution
First, check the file type
```console
file challenge.wav
```
> challenge.wav: RIFF (little-endian) data, WAVE audio, Microsoft PCM, 16 bit, mono 44100 Hz

We need to get the flag from the given audio file. Use the sox, audio processing tool to generate a spectrogram from challenge.wav and save it as an image.
```console
sox challenge.wav -n spectrogram -o challenge.png
```
Open challenge.png, you will see the flag:
![image](https://github.com/kqrrrr/Girls-In-CTF-2023/assets/95967644/636bba70-cf7c-4827-ad43-633eb0922e96)

## Flag
> GCTF2023{this_fl4g_sounds_weirddddddd}
