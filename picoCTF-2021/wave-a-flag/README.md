# Wave a flag

* Points: 10
* Category: General Skills

## Description

> Can you invoke help flags for a tool or binary? This program has extraordinarily helpful information...

## Solution

The description provides a download to the file "warm".

First we run the `file` command to find out more about the provided file:

```sh
file warm
```

```
warm: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=01b148cdedfc38125cac0d87e0537466d47927b1, with debug_info, not stripped
```

We discover that it is an executable file.

Before running the file, we can use the `strings` command and filter the output to try and find the flag:

```sh
strings warm | grep picoCTF
```

```
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_f0668f62}
```

## Flag

picoCTF{b1scu1ts_4nd_gr4vy_f0668f62}
