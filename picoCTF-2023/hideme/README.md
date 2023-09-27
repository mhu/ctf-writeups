# hideme

- Points: 100
- Category: Forensics, steganography

## Description

> Every file gets a flag.
>
> The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye here.

## Solution

First we check the file for hidden contents:

```bash
binwalk -e flag.png
```

```
DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 512 x 504, 8-bit/color RGBA, non-interlaced
41            0x29            Zlib compressed data, compressed
39739         0x9B3B          Zip archive data, at least v1.0 to extract, name: secret/
39804         0x9B7C          Zip archive data, at least v2.0 to extract, compressed size: 2959, uncompressed size: 3108, name: secret/flag.png
42998         0xA7F6          End of Zip archive, footer length: 22
```

It seems like there is a zip archive hidden in the image. So we extract it:

```bash
unzip flag.png
```

```
Archive:  flag.png
warning [flag.png]:  39739 extra bytes at beginning or within zipfile
  (attempting to process anyway)
   creating: secret/
  inflating: secret/flag.png
```

If we open the extracted image, we can see the flag written on it.

## Flag

picoCTF{Hiddinng*An_imag3_within*@n_ima9e_dc2ab58f}
