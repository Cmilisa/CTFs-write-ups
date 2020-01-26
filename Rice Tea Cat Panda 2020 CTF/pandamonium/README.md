# pandamonium

Category : General skills

Points : 100

## Description

AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA

91 7 10 D 95 42 28 A 

## Hints

underscore between 6th and 7th char, not including the flag wrapping (rtcp{})

## Solving

The tricky part is finding the cipher used, and realizing that the long chain of 'A's isn't some sort of key but just the challenge
author screaming. The things to get here is that the D and the A are not part of the cipher but actually given letters, and that the title
"pandamonium" has "amonium" in it, thus hinting about chemistry.

If we consider the given numbers are atomic numbers of chemical elements, we get :
* 91 : Protactinium abbreviated Pa
* 7 : Nitrogen / N
* 10 : Neon / Ne
* 95 : Americium / Am
* 42 : Molybdenum / Mo
* 28 : Nickel / Ni

Together they form the string `PaNNeDAmMoNiA`, and with it we can get the flag.

flag : rtcp{PaNNed_AmMoNiA}
