# Don't Give The GIANt a COOKie

Category : Cryptography

Points : 100

## Description

It was just a typical day in the bakery for Delphine. She was preparing her famous chocolate cake, when all of a sudden a GIANt burst through the doors of her establishment and demanded a cookie. Being the strong-willed girl she was, Delphine refused and promptly threw her rolling pin at the GIANt. Doing what any sensible being would do when faced with projectiles, the GIANt let out a shriek and ran out of the shop. Delphine smiled to herself, it was another day well done.

But oh? What's this? It seems the GIANt dropped this behind while he was screaming and scrambling out of the shop.

69acad26c0b7fa29d2df023b4744bf07

## Hint

This challenge still follows typical flag format, just wrap your answer with rtcp{answer_here}.

Non-case sensitive.

## Solving

The thing is to recognize that this is a md5 hash. Once that this is done, just use a hash cracker and you're done : 

![image](https://user-images.githubusercontent.com/57148042/73136402-7eaabe80-404d-11ea-8374-b1838e8d7f75.png)

Without forgetting to put it in the right format, we get the flag.

flag : rtcp{chocolate_mmm}
