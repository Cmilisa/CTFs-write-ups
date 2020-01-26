# notice me senpai

Category : Cryptography

Points : 100

## Description

uwu...senpai placed this note on my desk before class but i cant wead what it says!!!!!! can you hewp me????????? uwu tysm

tlyrc_o_0pnvhu}{137rmi__i_omwm

Challenge Author: Jess (the other one)/J

## Hint 

No hints.

## Solving

We can recognize in the given string some elements of the flag format, being left and right brackets, as well as underscores.
Looking further into it, we also notice the r, t, c and p letters. We can deduce of this that the flag is hidden in an anagram.
The twist is that there is leet speak into it, with the only ambiguity being the 1, that can represent a 'l' or an 'i', in this case
the latter.

To find the anagram we can use an angram solver, with rtcp{} removed from the string : 

![image](https://user-images.githubusercontent.com/57148042/73136636-f1b53480-404f-11ea-96fb-814e8142a5fd.png)

Now we just have to put back the flag together, along with the leet speak. After some time testing the different positions for the
numbers in the string, we get the flag.

flag : rtcp{im_1n_lov3_wi7h_y0ur_mom}
