# Allergic College Application

Category : Forensics

Points : 100

## Description

I was writing my common app essay in Mandarin when my cat got on my lap and sneezed. Being allergic, I sneezed with him, and when I blew my nose into a tissue, the text for my essay turned really weird! Get out, Bad Kitty!

## Hint

No hints

## Solving

First things first, let's open the given file content in any text editor. I'll use Atom, but any except notepad should do fine :

![image](https://user-images.githubusercontent.com/57148042/73185685-cc432c00-411e-11ea-824d-2860b7475ff5.png)

It's complete gibberish, but the challenge description hinted at something in Mandarin, so let's try to change the character encoding.
Luckily Atom has a encoding auto-detect function, so let's use it and see what we got :

![image](https://user-images.githubusercontent.com/57148042/73185755-ed0b8180-411e-11ea-99fe-1256d58f435d.png)

That's better. We can see the flag into brackets at the bottom. No need to translate anything, just enter the flag, with flag format, directly in Mandarin and we're done.

flag : rtcp{我_只_修改_了_两_次}
