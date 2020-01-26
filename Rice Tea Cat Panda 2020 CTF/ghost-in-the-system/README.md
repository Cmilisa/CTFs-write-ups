# ghost-in-the-system

Category : General skills

Points : 1500

## Description

I think my `ls` is being haunted... the colors are all weird!!! What's that? It's highlighting things?! Where!!?

## Hint

Flag is 100 characters long.
It starts with rtcp{ and ends with }
The first character is w

The flag is written in standard leet, the only exceptions are the flag wrapping (rtcp{}) and underscores (_)

## Solving

The challenge makes us download a modified version of ls, so let's do like reverse engineering challenges, and execute it :

![image](https://user-images.githubusercontent.com/57148042/73140168-1ae8bb80-4076-11ea-8691-f642004b418b.png)

Woah. Although very trippy, it doesn't seem to give us information, so let's open it with IDA, find the main function, and generate pseudo-code :

![image](https://user-images.githubusercontent.com/57148042/73140203-79159e80-4076-11ea-8bf0-ffa57676138a.png)

We can see a bit of the `ls` part of the binary, but what we are interested in is the long string in the middle of it. The string is accessed
right after that to populate an array called `flag` with characters. Pretty sneaky, huh ?

I imagine there could be smarter way, but let's dive in and get the flag in a straight forward and very manual way. Let's copy the string,
and the indices at which it is accessed to populate the `flag` array into a python script and let it do the work for us :

![image](https://user-images.githubusercontent.com/57148042/73140236-01943f00-4077-11ea-8d09-1b8710a13817.png)

And get the result :

![image](https://user-images.githubusercontent.com/57148042/73140241-1a045980-4077-11ea-81fa-e188a111b828.png)

flag : rtcp{wh37h3r_1n4n1m473_f16ur35_0r_un4u7h0r1z3d_c0d3_7h3r35_4lw4y5_4_6h057_1n_7h3_5y573m_1056_726_00}
