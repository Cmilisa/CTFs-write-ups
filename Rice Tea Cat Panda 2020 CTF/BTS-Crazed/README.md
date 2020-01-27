# BTS-Crazed

Category : Forensics

Points : 75

## Description

My friend made this cool remix, and it's pretty good, but everyone says there's a deeper meaning in the music. To be honest, I can't really tell - the second drop's 808s are just too epic.

## Hint

[Challenge input](https://github.com/JEF1056/riceteacatpanda/raw/master/BTS-Crazed%20(75)/Save%20Me.mp3)

## Solving

This challenge is pretty straight forward if you know a little about forensics. Just use the `strings 'Save me.mp3' | grep rtcp` to get the flag :

![image](https://user-images.githubusercontent.com/57148042/73187241-686e3280-4121-11ea-9469-7158855e4559.png)

flag : rtcp{j^cks0n_3ats_r1c3}
