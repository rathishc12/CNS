# Cryptography---19CS412-classical-techqniques


## Caeser Cipher

Caeser Cipher using with different key values

# AIM:

To develop a simple C program to implement Caeser Cipher.


## DESIGN STEPS:

### Step 1:

Design of Caeser Cipher algorithnm 

### Step 2:

Implementation using C or pyhton code

### Step 3:

Testing algorithm with different key values. 

## PROGRAM:
```
#include <stdio.h>
#include <string.h>

int main()
 {
    int key;
    char s[1000];

    printf("Enter a plaintext to encrypt:\n");
    fgets(s, sizeof(s), stdin);
    printf("Enter key:\n");
    scanf("%d", &key);

    int n = strlen(s);

    for (int i = 0; i < n; i++) 
    {
        char c = s[i];
        if (c >= 'a' && c <= 'z') 
        {
            s[i] = 'a' + (c - 'a' + key) % 26;
        }
        else if (c >= 'A' && c <= 'Z')
        {
            s[i] = 'A' + (c - 'A' + key) % 26;
        }
    }
    printf("Encrypted message: %s\n", s);

    for (int i = 0; i < n; i++)
    {
        char c = s[i];
        if (c >= 'a' && c <= 'z') 
        {
            s[i] = 'a' + (c - 'a' - key + 26) % 26; 
        }
        else if (c >= 'A' && c <= 'Z')
        {
            s[i] = 'A' + (c - 'A' - key + 26) % 26; 
        }
    }
    printf("Decrypted message: %s\n", s);

    return 0;
}

```

## OUTPUT:
![image](https://github.com/user-attachments/assets/40cc1fc3-4a68-4049-93d8-7dd61ea195fe)


## RESULT:
The program is executed successfully

