# Wireshark doo dooo do doo...

* Points: 50
* Category: Forensics

## Description

> Can you find the flag?

## Solution

We open the attached file in Wireshark and inspect the traffic. We can see that there are a lot of POST requests, but are there any GET requests (that might try to retrieve the flag)?

To filter the packets for only GET requests, we can use the filter `http.request.method == "GET"`.

We see only two requests. We inspect the response of the first request by clicking "Follow > TCP Stream".

The response body contains a string in a familiar format:

```
Gur synt vf cvpbPGS{c33xno00_1_f33_h_qrnqorrs}
```

This looks like a caesar cypher. If we shift every letter by 13 places, we find our flag.

## Flag

picoCTF{p33kab00_1_s33_u_deadbeef}
