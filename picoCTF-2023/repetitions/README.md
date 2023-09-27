# repetitions

- Points: 100
- Category: General Skills, base64

## Description

> Can you make sense of this file?
>
> Download the file here.

## Solution

First we take a look at the file:

```bash
cat enc_flag
```

```
VmpGU1EyRXlUWGxTYmxKVVYwZFNWbGxyV21GV1JteDBUbFpPYWxKdFVsaFpWVlUxWVZaS1ZWWnVh
RmRXZWtab1dWWmtSMk5yTlZWWApiVVpUVm10d1VWZFdVa2RpYlZaWFZtNVdVZ3BpU0VKeldWUkNk
MlZXVlhoWGJYQk9VbFJXU0ZkcVRuTldaM0JZVWpGS2VWWkdaSGRXCk1sWnpWV3hhVm1KRk5XOVVW
VkpEVGxaYVdFMVhSbFZrTTBKeldWaHdRMDB4V2tWU2JFNVdDbUpXV2tkVU1WcFhWVzFHZEdWRlZs
aGkKYlRrelZERldUMkpzUWxWTlJYTkxDZz09Cg==
```

It looks like a Base64 string, so we decode it:

```bash
cat enc_flag | base64 -d
```

```
VjFSQ2EyTXlSblJUV0dSVllrWmFWRmx0TlZOalJtUlhZVVU1YVZKVVZuaFdWekZoWVZkR2NrNVVX
bUZTVmtwUVdWUkdibVZXVm5WUgpiSEJzWVRCd2VWVXhXbXBOUlRWSFdqTnNWZ3BYUjFKeVZGZHdW
MlZzVWxaVmJFNW9UVVJDTlZaWE1XRlVkM0JzWVhwQ00xWkVSbE5WCmJWWkdUMVpXVW1GdGVFVlhi
bTkzVDFWT2JsQlVNRXNLCg==
```

The output still looks like a Base64 string, so we decode it again (and again, and again, ...)

```bash
cat enc_flag | base64 -d | base64 -d | base64 -d | base64 -d | base64 -d | base64 -d
```

```
picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_73494190}
```

## Flag

picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_73494190}
