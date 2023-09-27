# rotation

- Points: 100
- Category: Cryptography

## Description

> You will find the flag after decrypting this file
>
> Download the encrypted flag here.

## Solution

```bash
cat encrypted.txt
```

```
xqkwKBN{z0bib1wv_l3kzgxb3l_i4j7l759}
```

It looks like a string encoded with a Caesar cipher. We try different shifts until we get the flag. In this case we get the solution with n = 18.

## Flag

picoCTF{r0tat1on_d3crypt3d_a4b7d759}
