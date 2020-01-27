# catch-at

Category : Forensics

Points : 66

## Description

636274425917865984

## Hint

No hints

## Solving

This challenge is the continuation of the cat-chat challenge. We already found the flag to this challenge in the previous one, but let's
see the actual method for this one. The description hints at a discord functionality, so let's enable the developper mode in the options.
This mode allows us to get the ids of users, servers, channels, and what we are intereset in here, messages.

By right clicking on them, we can get the ids of the rtcp discord server `624036526157987851`, the `#catchat` channel `633364891616411667`. 
From these ids we can craft a url that points the server's channel : `https://discordapp.com/channels/624036526157987851/633364891616411667`.
We then just need to add the message id we are given to it : `https://discordapp.com/channels/624036526157987851/633364891616411667/636274425917865984`.

Let's click on it, and it brings us directly to the message that contains the flag :

![image](https://user-images.githubusercontent.com/57148042/73185098-c436bc80-411d-11ea-8e3e-ffb8e0d8d89f.png)

Which reads : `OH BY THE WAY, HERE'S A LITTLE SOMETHING: W0W_D15C0RD_H4S_S34RCH_F34TUR35`. Put back the flag format and we're done.

flag : rtcp{W0W_D15C0RD_H4S_S34RCH_F34TUR35}
