# Mod 26

* Points: 10
* Category: Cryptography

## Description

> Cryptography can be easy, do you know what ROT13 is?
>
>`cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_hyLicInt}`

## Solution

We can use Python's codecs module to decode the string:

```python
import codecs

print(codecs.decode("cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_hyLicInt}", "rot_13"))
```

```
picoCTF{next_time_I'll_try_2_rounds_of_rot13_ulYvpVag}
```

## Flag

picoCTF{next_time_I'll_try_2_rounds_of_rot13_ulYvpVag}
