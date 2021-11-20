# information

* Points: 10
* Category: Forensics

## Description

> Files can always be changed in a secret way. Can you find the flag?

## Solution

The description provides a download to the file "cat.jpg".

To find out more about the file, we first run `file cat.jpg`:

```
cat.jpg: JPEG image data, JFIF standard 1.02, aspect ratio, density 1x1, segment length 16, baseline, precision 8, 2560x1598, components 3
```

It seems to be a regular JPEG file. For more information, we can use `exiftool`.

```sh
exiftool cat.jpg
```

```
ExifTool Version Number         : 12.34
File Name                       : cat.jpg
Directory                       : .
File Size                       : 858 KiB
File Modification Date/Time     : 2021:03:15 14:24:46-04:00
File Access Date/Time           : 2021:11:19 20:34:26-05:00
File Inode Change Date/Time     : 2021:11:19 20:34:21-05:00
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.02
Resolution Unit                 : None
X Resolution                    : 1
Y Resolution                    : 1
Current IPTC Digest             : 7a78f3d9cfb1ce42ab5a3aa30573d617
Copyright Notice                : PicoCTF
Application Record Version      : 4
XMP Toolkit                     : Image::ExifTool 10.80
License                         : cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9
Rights                          : PicoCTF
Image Width                     : 2560
Image Height                    : 1598
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 2560x1598
Megapixels                      : 4.1

```

The license looks suspicious. Because it looks like a Base64 string, we should try to decode it:

```sh
echo "cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9" | base64 -d
```

```
picoCTF{the_m3tadata_1s_modified}
```

## Flag

picoCTF{the_m3tadata_1s_modified}
