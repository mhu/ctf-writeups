# Nice netcat...

* Points: 15
* Category: General Skills

## Description

> There is a nice program that you can talk to by using this command in a shell: `$ nc mercury.picoctf.net 21135`, but it doesn't speak English...

## Solution

Running `nc mercury.picoctf.net 21135` gives us the following output:

```
112
105
99
111
67
84
70
123
103
48
48
100
95
107
49
116
116
121
33
95
110
49
99
51
95
107
49
116
116
121
33
95
97
102
100
53
102
100
97
52
125
10
```

If we save the output in a file called `flag.txt`, we can use Python to load it and work out a solution.

```python
with open("flag.txt", "r") as f:
    flag = [int(n) for n in f.readlines()]
```

First, we should check what the Unicode representation of our list looks like:

```
unicode = [chr(n) for n in flag]
print(unicode)
```

```
['p', 'i', 'c', 'o', 'C', 'T', 'F', '{', 'g', '0', '0', 'd', '_', 'k', '1', 't', 't', 'y', '!', '_', 'n', '1', 'c', '3', '_', 'k', '1', 't', 't', 'y', '!', '_', 'a', 'f', 'd', '5', 'f', 'd', 'a', '4', '}', '\n']
```

We can see that this must be our flag. To make it more readable, we can convert our list to a string:

```python
print(''.join(unicode))
```

```
picoCTF{g00d_k1tty!_n1c3_k1tty!_afd5fda4}
```

## Flag

picoCTF{g00d_k1tty!_n1c3_k1tty!_afd5fda4}
