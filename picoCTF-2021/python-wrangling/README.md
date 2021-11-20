# Python Wrangling

* Points: 10
* Category: General Skills

## Description

> Python scripts are invoked kind of like programs in the Terminal... Can you run this Python script using this password to get the flag?

## Solution

The description provides downloads to three files: "ende.py", "pw.txt" and "flag.txt.en".

First we try running the Python script:

```sh
python ende.py
```

```
Usage: ende.py (-e/-d) [file]
```

If we assume that `-e` stands for "encode" and that `-d` stands for "decode", we can try the following:

```sh
python ende.py -d flag.txt.en
```

The script is asking us for a password. We run it again, this time passing the password from "pw.txt":

```sh
cat pw.txt | python ende.py -d flag.txt.en
```

This time the script prints the flag after receiving our input:

```
Please enter the password:picoCTF{4p0110_1n_7h3_h0us3_ac9bd0ff}
```

## Flag

picoCTF{4p0110_1n_7h3_h0us3_ac9bd0ff}
