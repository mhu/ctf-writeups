# who is it

- Points: 100
- Category: Forensics, email

## Description

> Someone just sent you an email claiming to be Google's co-founder Larry Page but you suspect a scam.
>
> Can you help us identify whose mail server the email actually originated from?
>
> Download the email file here. Flag: picoCTF{FirstnameLastname}

## Solution

First we print the file:

```bash
cat email-export.eml
```

We see the following suspcious looking line multiple times.

```
google.com: domain of lpage@onionmail.org designates 173.249.33.206 as permitted sender
```

We can use a whois lookup to find out more about the IP address. We visit https://www.whois.com/whois/173.249.33.206.

On the website we see the following information:

```
person: Wilhelm Zwalina
```

## Flag

picoCTF{WilhelmZwalina}
