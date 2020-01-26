# Pandas Like Salads 

Category : Cryptography

Points : 350

## Description

Did you know a new panda was added to the Washington DC zoo recently? Yep, apparently she really like salads. Interesting, yeah? Also, the panda keepers of the zoo said that the key to happiness in life is a little CUTENESS every day. You know, all the keepers who are on the panda's rotation all said the same thing to me. Very interesting.

## Hint

No hints.

## Solving

This time one png file is given with the challenge, which contains some message written in a weird alphabet. By searching around 
[Dcode](https://dcode.fr) we find that the alphabet used is the pig pen alphabet, and we translate it : 

![image](https://user-images.githubusercontent.com/57148042/73136973-f54aba80-4053-11ea-9330-a5707b8f4846.png)

We can immediatly notice that the resulting string is still encoded, and that where the "rtcp" flag should be contains twice the same letter.
The second thing to nice is that the challenge description mentions that "the **key** to happiness in life is a little **CUTENESS** every day". It also mentions some kind of rotation.

We can then suppose it is either Vigenere, ROT, or a combinaison of both. We then try Vigenere cipher and it's variations. (the right one to use there is the Variant Beaufort cipher)
There is a slight trick here, we need to encode, and not decode the cipher for it to give us the right answer : 

![image](https://user-images.githubusercontent.com/57148042/73137169-9e45e500-4055-11ea-85e8-431e8c4a15af.png)

We can then brute force the rot cipher, and see that this was rot-21 : 

![image](https://user-images.githubusercontent.com/57148042/73137194-d8af8200-4055-11ea-9978-ac6548d05e12.png)

flag : RTCP{PANDAS_SHOULD_NOT_BE_PUT_IN_PENS}
