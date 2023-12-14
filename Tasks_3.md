Task 1:

The binary program witch checks the password 

Password compares with the string that generates with the two byte arrays.

```python
x = [0x50, 0xB3, 0x67, 0xAF, 0xA5, 0x0E, 0x77, 0xA3, 0x4A, 0xA2, 0x9B, 0x01, 0x7D, 0x89, 0x61, 0xA5, 0xA5, 0x02, 0x76, 0xB2, 0x70, 0xB8, 0x89, 0x03, 0x79, 0xB8, 0x71, 0x95, 0x9B, 0x28, 0x74, 0xBF, 0x61, 0xBE, 0x96, 0x12, 0x47, 0x95, 0x3E, 0xE1, 0xA5, 0x04, 0x6C, 0xA3, 0x73, 0xAC, 0x89, 0x00]
y = [0x18, 0xd6, 0x15, 0xca, 0xfa, 0x77, 0x00, 0x00]
```

With the following algorithm : 
```python
i = 0
while True:
    if x[i] == 0x00:
        break
    key.append(x[i] ^ y[i + len(y)])
```

The resulting key is following

```python
key = ['H', 'e', 'r', 'e', '_', 'y', 'w', '£', 'R', 't', '\x8e', 'Ë', '\x87', 'þ', 'a', '¥', '½', 'Ô', 'c', 'x', '\x8a', 'Ï', '\x89', '\x03', 'a', 'n', 'd', '_', 'a', '_', 't', '¿', 'y', 'h', '\x83', 'Ø', '½', 'â', '>', 'á', '½', 'Ò', 'y', 'i', '\x89', 'Û', '\x89']
```

Task 2:

task 2 is bin program with custom input and output but the logic is simple.
The program trys to get correct username and password.

The right username is `john` and the password is `the ripper`.