# No sleep

Category : Web

Points : 100

## Description

Jess doesn't get enough sleep, since he's such a gamer so in this challenge, you'll be staying up with him until 4:00 in the morning :D on a Monday! Let's go, gamers!

## Hint

[Challenge](https://riceteacatpanda.wtf/onlyrealgamers)

## Solving

The challenge greats us with a countdown that ends in a few days, but as we may get the flag at the end of the countdown, we want the flag now !
Fortunately for us, the countdown is in javascript, so let's open up the developper tools to take a look at it :

![image](https://user-images.githubusercontent.com/57148042/73142285-43c87b00-408d-11ea-9fbd-e7f58cf9139a.png)

It looks like it's obfuscated a bit, so let's pass it into the js beautifier :

![image](https://user-images.githubusercontent.com/57148042/73142352-cfdaa280-408d-11ea-8135-441b1895f785.png)

Here we can see we have an array where the elements are probably part of the obfuscation of methods. After that there is a function that
seem to shift the array repeatedly, so if we're going to replace array accessing with actual methods we are going to need to see in which order
the array lands after this function. There is also another small function that simply accesses the elements of the array.

After that we have the part of the code that handles the timer and its display in days, hours, minutes and seconds, which is not very
important here. Last, there is CryptoJS that is used, probably with the long string present in the array.

So let's get the actual order of the array. The parametter passed into the function is `0x99` which is 153. (this value is incremented
inside the function, but is decremented in the while loop before the condition check like so : `while (--_0x2d3fd2)` so the right value to take
is 153)
The length of the array is 14, and we have `154 / 14 = 11`, so 153 is just short of 11 whole rotations of the array. That means that we
just end up with the last element on front, which is `cookie`.

Deobfuscating the CryptoJS line we get `var decoded = CryptoJS.AES.decrypt('U2FsdGVkX18kRm6FDkRVQfVuNPTxyOnJzpu8QnI/9UKoCXp6hQcley11nBnLIItj', 'ok boomer')`,
and the line after it `document.getElementById('gamer timer').innerHTML = decoded.toString(CryptoJS.enc.Utf8)`.

We then just need to execute the js code and get the flag.

One could have noticed that we just need to reach the timer to get the flag, and that the date was stored into a cookie, thus only
needing to modify the cookie at the right date.

flag : rtcp{w0w_d1d_u_st4y_up?}
