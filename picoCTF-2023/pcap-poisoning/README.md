# PcapPoisoning

- Points: 100
- Category: Forensics, pcap

## Description

> How about some hide and seek heh?
>
> Download this file and find the flag.

## Solution

The description includes a link to a PCAP file. Although the file is supposed to be opened with Wireshark, we can run `strings` first to see if there is anything interesting in the file.

```bash
strings trace.pcap
```

We see a lot of uninteresting output, but we also find the flag:

```
picoCTF{P64P_4N4L7S1S_SU55355FUL_5b6a6061}
```

## Flag

picoCTF{P64P_4N4L7S1S_SU55355FUL_5b6a6061}
