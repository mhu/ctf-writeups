# MacroHard WeakEdge

* Points: 60
* Category: Forensics

## Description

> I've hidden a flag in this file. Can you find it?

## Solution

The description provides a download to the file "Forensics is fun.pptm".

We begin by running the `file` command on the file:

```sh
file Forensics\ is\ fun.pptm
```

```
Forensics is fun.pptm: Microsoft PowerPoint 2007+
```

Next we use `binwalk` to extract any files that might be embedded in our target file:

```sh
binwalk -e Forensics\ is\ fun.pptm
```

`binwalk` created a new directory called "_Forensics is fun.pptm.extracted". We use `ls` to list its contents.

```sh
ls -l _Forensics\ is\ fun.pptm.extracted/
```

```
total 124
-rw-r--r-- 1 kali kali 100093 Nov 20 13:40  0.zip
-rw-r--r-- 1 kali kali  10660 Jan  1  1980 '[Content_Types].xml'
drwxr-xr-x 2 kali kali   4096 Nov 20 13:40  docProps
drwxr-xr-x 7 kali kali   4096 Nov 20 13:40  ppt
drwxr-xr-x 2 kali kali   4096 Nov 20 13:40  _rels
```

We see multiple directories and files. Because it could potentially be very time-consuming to search each directory one by one, we can try to list all subdirectories recursively:

```sh
ls -R _Forensics\ is\ fun.pptm.extracted/
```

```
'_Forensics is fun.pptm.extracted/ppt/slideMasters':
hidden  _rels  slideMaster1.xml
```

The output reveals a file called "hidden".

```sh
cat _Forensics\ is\ fun.pptm.extracted/ppt/slideMasters/hidden
```

```
Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q
```

The output looks like a Base64 encoded string separated by spaces. We can use the `tr` command to remove all spaces and the `base64` command to decode it:

```sh
cat _Forensics\ is\ fun.pptm.extracted/ppt/slideMasters/hidden | tr -d " " | base64 -d
```

```
flag: picoCTF{D1d_u_kn0w_ppts_r_z1p5}base64: invalid input
```

`base64` appends "base64: invalid input", since the input actually has an incorrect padding. Adding two "=" at the end would fix this problem:

```sh
echo "ZmxhZzogcGljb0NURntEMWRfdV9rbjB3X3BwdHNfcl96MXA1fQ==" | base64 -d
```

```
flag: picoCTF{D1d_u_kn0w_ppts_r_z1p5}
```

## Flag

picoCTF{D1d_u_kn0w_ppts_r_z1p5}
