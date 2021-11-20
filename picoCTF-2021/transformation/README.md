# Transformation

* Points: 20
* Category: Reverse Engineering

## Description

> I wonder what this really is... enc `''.join([chr((ord(flag[i]) << 8) + ord(flag[i + 1])) for i in range(0, len(flag), 2)])`

## Solution

The description provides a download to the file "enc".

The first thing we want to do is to check what kind of file we got:

```sh
file enc
```

```
enc: UTF-8 Unicode text, with no line terminators
```

It seems to be a regular text file. Let's print it:

```sh
cat enc
```

```
灩捯䍔䙻ㄶ形楴獟楮獴㌴摟潦弸彤㔲挶戹㍽
```

The description also provides us a bit of Python code. If we open the "enc" file in Python and pass it to the Python snippet, we get the following error:

```python
with open("enc", "r") as f:
  flag = f.read()

print(''.join([chr((ord(flag[i]) << 8) + ord(flag[i + 1])) for i in range(0, len(flag), 2)]))
```

```
Traceback (most recent call last):
  File "solve.py", line 6, in <module>
    print(''.join([chr((ord(flag[i]) << 8) + ord(flag[i + 1])) for i in range(0, len(flag), 2)]))
  File "solve.py", line 6, in <listcomp>
    print(''.join([chr((ord(flag[i]) << 8) + ord(flag[i + 1])) for i in range(0, len(flag), 2)]))
ValueError: chr() arg not in range(0x110000)
```

Some value that gets passed to `chr()` is too big.

Also, if we take a closer look at the snippet, we can see that it adds the `ord()` values of some string pairwise. Since our provided string has an odd number of characters (`len(flag)` will prove this), it is unlikely that the snippet will work with our input string.

What if our "enc" is not our input, but the output? To test this, we have to find a way to reverse our code.

The code uses list comprehension to continually add two numbers and get the Unicode representation of the sums. To revert `chr()` we will use `ord()`.

```python
print([ord(n) for n in flag])
```

```
[28777, 25455, 17236, 18043, 12598, 24418, 26996, 29535, 26990, 29556, 13108, 25695, 28518, 24376, 24420, 13618, 25398, 25145, 13181]
```

Because we have to split each number into two numbers and bit shift one of them, we first represent all of the numbers in their binary form:

```python
print([bin(ord(n)) for n in flag])
```

```
['0b111000001101001', '0b110001101101111', '0b100001101010100', '0b100011001111011', '0b11000100110110', '0b101111101100010', '0b110100101110100', '0b111001101011111', '0b110100101101110', '0b111001101110100', '0b11001100110100', '0b110010001011111', '0b110111101100110', '0b101111100111000', '0b101111101100100', '0b11010100110010', '0b110001100110110', '0b110001000111001', '0b11001101111101']
```

Because one of the summands is bit shifted by 8, we can just split the binary sum into two numbers: The last 8 bits represent one of the summands, the remaining bits represent the other summand (not bit shifted).

Example for the first two numbers:

```
we split the sum here
       v
1110000 01101001 -> 1110000 and 01101001
1100011 01101111 -> 1100011 and 01101111
```

Finally, we need to get the Unicode representation of our numbers. We turn the binary numbers into decimal numbers and pass them to `chr()`.

```python
for l in flag:
  original = ord(l)                # output character to decimal number
  original = str(bin(original))    # decimal number to binary number (as a string, so we can split the number easily)

  num1 = original[2:-8]            # slice the number to get the first summand (and omit the "0b" from the start of the string)
  num2 = original[-8:]             # slice the number to get the second summand

  print(chr(int(num1, 2)), end="") # print the Unicode representation of the first summand
  print(chr(int(num2, 2)), end="") # and the second
```

```
picoCTF{16_bits_inst34d_of_8_d52c6b93}
```

## Flag

picoCTF{16_bits_inst34d_of_8_d52c6b93}
