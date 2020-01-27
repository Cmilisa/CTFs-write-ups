# Uwu?

Category : Web

Points : 125

## Description

ᵘʷᵘ oh no ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ hecc sorry guys ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ sorry im dropping ᵘʷᵘ my uwus all over the ᵘʷᵘ place ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ oh no I lost one ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ

ah, Jake, you idiot

## Hint

[Challenge input](https://riceteacatpanda.wtf/uwu)

This challenge gets progressively harder the faster your internet is if you do it manually

## Solving

This challenge indeed needs us to slow things down, but let's go the easier way and simply use burp suite in intercept mode. Load the challenge
page, forward a few requests and see what we got :

![image](https://user-images.githubusercontent.com/57148042/73199262-cbb59000-4134-11ea-9f5a-6a054fe4c066.png)

It looks like the page got redirected a few times along the way. We can look them up one by one, but the one page that got what we're
interested in is `/you-better-wash-your-rice`. Search for "rtcp" and here it is :

![image](https://user-images.githubusercontent.com/57148042/73199403-16370c80-4135-11ea-9b7a-fa079b784b77.png)

flag : rtcp{uwu_,_1_f0und_y0u}
