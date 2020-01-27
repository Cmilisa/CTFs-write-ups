# cat-chat

Category : Forensics

Points : 125

## Description

nyameowmeow nyameow nyanya meow purr nyameowmeow nyameow nyanya meow purr nyameowmeow nyanyanyanya nyameow meow purr meow nyanyanyanya nya purr nyanyanyanya nya meownyameownya meownyameow purr nyanya nyanyanya purr meowmeownya meowmeowmeow nyanya meownya meowmeownya purr meowmeowmeow meownya purr nyanyanyanya nya nyameownya nya !!!!

## Hint

once you've figured this out, head to discord's #catchat channel.

## Solving

The thing to notice for this challenge, is that we only have three words being used here : 'nya', 'meow', and 'purr'. Also,
the 'purr' word is always used alone, and if we look at the #catchat channel on discord, we can also notice that the 'purr' word is never
used on front. With these informations, we can deduce (the pronunciation of those words hint at this as well) that this code is
indeed morse code. 'nya's correpond to dots, 'meow's to dashes, and 'purr's to stops. We can then make a python script to translate it for us,
and get :

![image](https://user-images.githubusercontent.com/57148042/73183613-61dcbc80-411b-11ea-8925-5a5bc107c28c.png)

Now that we got this, let's head to the discord channel mentioned before. Here the is a conversation writte a cat-chat to translate. Two solutions are available, either translate each messages
one by one until we found the flag, but this one is tedious as there are a lot of messages. The other solution is to simply copy
all the messages, and search for the '_' character in cat-chat, as it should only be used in the flag we are looking for. Doing this we
find actually to instances of multiple underscores next to each other. The first one :

![image](https://user-images.githubusercontent.com/57148042/73184113-34444300-411c-11ea-872c-b4c8bc204cc5.png)

Which translate to `RTCP:TH15_1Z_A_C4T_CH4T_N0T_A_M3M3_CH4T`, that we just need to put back into flag format. The second one is :

![image](https://user-images.githubusercontent.com/57148042/73184217-5fc72d80-411c-11ea-8f46-e8c2868b95d7.png)

Which translates to `OH BY THE WAY, HERE'S A LITTLE SOMETHING: W0W_D15C0RD_H4S_S34RCH_F34TUR35`. This is the flag for the second
cat-chat related challenge. (see catch-at)

flag : rtcp{TH15_1Z_A_C4T_CH4T_N0T_A_M3M3_CH4T}
