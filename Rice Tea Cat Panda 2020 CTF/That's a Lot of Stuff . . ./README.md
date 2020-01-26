# That's a Lot of Stuff . . .

Category : Cryptography

Points : 275

## Decription 

31 34 33 20 31 35 36 20 31 32 32 20 31 35 32 20 31 34 33 20 31 31 30 20 31 36 34 20 31 35 32 20 31 31 35 20 31 30 37 20 36 35 20 36 32 20 31 31 35 20 36 33 20 31 31 32 20 31 37 32 20 31 31 35 20 31 32 34 20 31 30 32 20 31 36 35 20 31 34 33 20 36 31 20 37 31 20 31 35 30 20 31 34 33 20 31 35 32 20 31 31 36 20 31 34 36 20 31 31 36 20 31 30 36 20 37 31 20 31 35 32 20 31 31 35 20 31 30 34 20 31 30 32 20 31 31 35 20 31 33 30 20 36 32 20 31 31 35 20 36 30 20 31 34 34 20 31 31 30 20 31 31 36 20 37 31

## Hint

No hints

## Solving

Although this one is not particularly clear, it turns out that this is hexadecimal. To decode it we are going to use the very
usefull cyberchef tool :

![image](https://user-images.githubusercontent.com/57148042/73136749-78b6dc80-4051-11ea-84f8-2e6d54eeb06c.png)

The result is still encoded, so we're not finished yet. Here we can notice that not a single digit is above 8, so we can (rightfully) assume that this is octal encoded : (be carefull though, as cyberchef separates base8 and octal, and the results are different if you used base8)

![image](https://user-images.githubusercontent.com/57148042/73136788-d4816580-4051-11ea-8ba9-3268eaa7d6ee.png)

Still encoded ! This time the encoding is pretty clear, it's base 64, so let's use cyberchef one last time : 

![image](https://user-images.githubusercontent.com/57148042/73136799-ff6bb980-4051-11ea-8ab5-c756dd6e2612.png)

flag : rtcp{c0nv3rs10ns_ar3_4_c00L_c4ts}
