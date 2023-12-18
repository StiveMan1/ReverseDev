Simple program that checks password given like argument of the program

Program is compiled in gcc compiler
The program consist of three steps
1. Check the input password to be lower upper cases and numbers
2. Copy the given password
3. Generate password to compare with copied password

The correct password is `ff07031d6fb052490149f44b1d5e94f1592b6bac93c06ca9`


The Generation start with the initial string `THEPASSWORDISEASYTOCRACK`

```c++
void password_generation_function(char* _data, char* result) {

    _data[0] =  _data[0] ^ 0xab;
    char* pointer = _data + 1;
    char chr = *pointer;
    if (chr != 0) {
        int counter = 1;
        do {
            chr = chr - counter;
            pointer[0] = chr;
            
            chr = chr ^ _data[(counter - 1)];
            pointer[0] = chr;
            
            chr = chr + _data[(counter - 1)];
            pointer[0] = chr;
            
            chr = chr ^ _data[(counter - 1)];
            pointer[0] = chr;
            
            chr = chr ^ _data[8];
            pointer[0] = chr;
            if (chr == 0)  pointer[0] = 1;
            
            pointer = _data + ++counter;
            chr = _data[counter];
        } while (chr != 0);
    }
    unsigned value = *_data;
    while (value != 0) {
        sprintf(result, "%.2x", value);
        result += 2;
        value = *(unsigned char *) ++ _data;
    }
}
```

