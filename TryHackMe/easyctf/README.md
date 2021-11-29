# Simple CTF

* Link: https://tryhackme.com/room/easyctf
* Difficulty: Easy
* Points: 300

> How many services are running under port 1000?

```sh
nmap -sV 10.10.114.110
```

**Answer**: 2

> What is running on the higher port?

**Answer**: ssh

> What's the CVE you're using against the application?

**Answer**: CVE-2019-9053

> To what kind of vulnerability is the application vulnerable?

**Answer**: sqli

> What's the password?

**Answer**: secret

> Where can you login with the details obtained?

**Answer**: ssh

> What's the user flag?

**Answer**: G00d j0b, keep up!

> Is there any other user in the home directory? What's its name?

**Answer**: sunbath

> What can you leverage to spawn a privileged shell?

**Answer**: vim

> What's the root flag?

**Answer**: W3ll d0n3. You made it!
