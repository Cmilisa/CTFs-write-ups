# Code on

Category : Cryptography

Points : 500

## Description

My houseplant and I were working on a biology assignment together. Yes, my houseplant. Don't question it. Anyways, she ended up giving me a new cipher to use in my next project! So I'm giving it to my biology friends to see if they can solve it. They are, after all, studying DNA and mRNA right now.

```
AUGCAAGGUCUCUUGACCCAGUGGAUACUAAAUGCCUGGAAGGUAGCAUACUAG

Key: 6, 3, 4, 3, 1, 9, 8, 3, 3, 2, 7, 4, 1, 2, 4, 1
```

## Hint

Make sure to encase the plaintext with rtcp{} Spaces are represented by a underscore, (_)

## Solving

By looking at the challenge description and the input we got we can immediatly guess that this has to do with biology, and more specifically
DNA and mRNA. Using the [Dcode](https://www.dcode.fr/codons-genetic-code) tool for that purpose we get a string of amino acids :

![image](https://user-images.githubusercontent.com/57148042/73137289-dc8fd400-4056-11ea-9e0c-e2615bd96238.png)

One thing to notice here is that we get 17 amino acids, and that the length of the key is 16. That means that if we want to match
each part of the key with an amino acids, we have to take the "KEY" word into the key, shifting all numbers one amino acid to the right.
(and in reality discard the first amino acid)

One could also say the AUG code for mRNA is actually the start codon, but i only knew this afterwards.

The numbers then refer to a letter in the complete name of the amino acid, which is the letter at the position indicated by the number
associated to it. Combining all that we get the string "mycutehouseplant", which we then put back into the right format and get the flag.

flag : rtcp{my_cute_houseplant}
