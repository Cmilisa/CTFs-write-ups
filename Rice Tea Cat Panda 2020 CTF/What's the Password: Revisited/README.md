# What's the Password: Revisited

Category : Reverse Engineering

Points : 300

## Description

There's a password somewhere...

## Hint

No hints

## Solving

This is a reverse engineering challenge, so first things first, let's execute it and see what it does. (of course, this one should
cause no harm, but always execute those kind of binaries inside a virtual environment)

The binary asks us for a password, we enter one, and it turns out it's not the right one. Now, let's bring in the tool. I choose
IDA as it usually gives me more information than the other ones, but any reverse engineering tool should be good enough.
We can work through the assembly, but lucky for us IDA got a pseudo-code generator, so let's use it :

![image](https://user-images.githubusercontent.com/57148042/73139137-2aaed280-406b-11ea-8d09-4b5028df048c.png)


We can see the line where the binary asks for a password, the line that gets our guess, and we can even notice a buffer overlow protection
at the end.

What we are really interested in though is the for loop in the middle. It loops over 20 indices, and compares some array in memory
to what we entered, with a twist. First let's look at the `byte_201020` location in memory :

![image](https://user-images.githubusercontent.com/57148042/73139253-5aaaa580-406c-11ea-81ab-0fb11a97ce1f.png)

We can clearly see that this is a string. Now let's look at what happens to our input. The first thing to notice is that it is
accessed with the same indices as the string we just found, so the length of the password should be the same, that is 20 characters.

Next we see that each character is XORed with the hexadecimal value 0x32, then added one, and then XORed again. This is easily reversable,
so let's do it, and make it a python script : (remember that the inverse operation of an XOR is the same XOR)

![image](https://user-images.githubusercontent.com/57148042/73139289-dc9ace80-406c-11ea-8a66-3835ff3183ab.png)

Now execute the string and we get our password :

![image](https://user-images.githubusercontent.com/57148042/73139297-f3d9bc00-406c-11ea-82c9-315b24be9707.png)

Last step, input the password into the binary, and get the flag : 

![image](https://user-images.githubusercontent.com/57148042/73139358-867a5b00-406d-11ea-8bff-3784f4862afb.png)

flag : rtcp{fL492_r_50m371m32\5Pr34D_0U7}
