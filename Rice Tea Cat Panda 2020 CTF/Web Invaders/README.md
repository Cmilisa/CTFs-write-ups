# Web Invaders

Category : Web

Points : 250

## Description

[Challenge input](https://jef1056.github.io/)

## Hint

No hints.

## Solving

This challenge can be solved in 2 ways, the first being the same as Tea Clicker using Cheat Engine, so let's cover the one instead.
Open up the Web Invaders page, bring in the developper tools, go in the network tab and reload the page :

![image](https://user-images.githubusercontent.com/57148042/73197209-3664cc80-4131-11ea-8a53-c10d44a83dbc.png)

The request we are interested in here is the one with the `game.arcd0` file. Let's look at the response, which is encoded in base64,
decode it and let's search the string "rtcp" in it :

![image](https://user-images.githubusercontent.com/57148042/73197507-b0955100-4131-11ea-8f17-b80777ac398c.png)

flag : rtcp{web_h^ck3r_0004212}
