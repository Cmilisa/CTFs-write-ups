# Tea clicker

Category : Binary/Executable

Points : 150

## Description

It's not too far back in my memory when cookie clickers were all the rage. But this new one with tea and cats has such great art and themes, I'm hooked! Unfortunately, the only reward is so many clicks away, and even if I spend double the time, I still can't get it!

## Hint

[Challenge input](https://github.com/JEF1056/riceteacatpanda/raw/master/Tea Clicker (150)/Tea Clicker.zip)

## Solving

As always, first things first, let's launch the challenge's executable. We get greeted by a clicker game, with a enormous score to
reach. Oh and macros or bots don't work, so we'll have to find another way.

![image](https://user-images.githubusercontent.com/57148042/73192523-7031d500-4129-11ea-99f6-c850d169be2b.png)

Let's use Cheat Engine for that. Open it up and attach it to Tea Clicker's process. There are 2 methods to get the flag, but let's
take the long way first.

To get the flag, we need to modify our score to meet the requirement set by the game. So we'll do a Cheat Engine scan, with all value types,
and unknown initial value (even if our score is 0, it may not be stored as a 0 in the memory)

![image](https://user-images.githubusercontent.com/57148042/73193411-d10ddd00-412a-11ea-8ca4-bde01c74c670.png)

Next let's do some "Unchanged value" scans. We are not modifying our score so its value in memory should stay unchanged as well.
Then click to get the score up by 1, then one scan with "Changed value", then some more "Unchanged value" scans to trim out the matches we got.

![image](https://user-images.githubusercontent.com/57148042/73194038-d0c21180-412b-11ea-82af-24c0781b18ef.png)

We are down to ~28.000, so let's do a few more rounds of changed/unchanges value scans until we just a few possibilities left.

![image](https://user-images.githubusercontent.com/57148042/73194191-1252bc80-412c-11ea-851c-7f4f27c0d3c7.png)

We can see we have a potential candidate to our score variable, as it matches with our actual score. So let's try to change its
value to something bigger :

![image](https://user-images.githubusercontent.com/57148042/73194383-6bbaeb80-412c-11ea-90a0-8830623d39cd.png)

And here we go :

![image](https://user-images.githubusercontent.com/57148042/73194457-88efba00-412c-11ea-8f7a-7e0e81be148c.png)

Another way of doing this was to hit the "Memory view" button just underneath the scans results and directly search for "rtcp{" :

![image](https://user-images.githubusercontent.com/57148042/73194647-d0764600-412c-11ea-88ba-a7a72eccbc22.png)

flag : rtcp{w0w_ur_5uch_a_t2^_g^m3r}
