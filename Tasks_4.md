Task 1:

filename ch19.pyc
I decompiled it into a classic Python ".py" file.
The code is obtained from single line input.

```python
KEY = 'I know, you love decrypting Byte Code !'
I = 5
for X in PASS:
    KEYOUT.append((ord(X) + I ^ ord(KEY[I])) % 255)
    I = (I + 1) % len(KEY)
```

Then use this code to modify the original string and compare it to a Python array.

```python
KEYOUT = [57, 73, 79, 16, 18, 26, 74, 50, 13, 38, 13, 79, 86, 86, 87]
```

The flag is `I_hate_RUBY_!!!`

Task 2:

The second task is windows game names "Crackme v0.1".
The task is to reach the white platform above.
My hypothesis is that you can change the jump height in a binary file.