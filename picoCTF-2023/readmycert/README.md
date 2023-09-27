# ReadMyCert

- Points: 100
- Category: Cryptography

## Description

> How about we take you on an adventure on exploring certificate signing requests
>
> Take a look at this CSR file here.

## Solution

We can use the following command to view the contents of the CSR file:

```bash
openssl req -in readmycert.csr -noout -text
```

## Flag

picoCTF{read_mycert_57f58832}
