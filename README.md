# Cryptography --- 19CS412 - Advanced Encryption Standard DES Algorithm

# EXP - 7 ADVANCED ENCRYPTION STANDARD DES ALGORITHM

## AIM:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

## ALGORITHM: 
  1. AES is based on a design principle known as a substitution–permutation. 
  2. AES does not use a Feistel network like DES, it uses variant of Rijndael. 
  3. It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits. 
  4. AES operates on a 4 × 4 column-major order array of bytes, termed the state

## PROGRAM: 
Program to implement Advanced Encryption Standard DES Algorithm.

Developed by : KEERTHIVASAN S

Register Number : 212223220046

```
#include <stdio.h>
#include <string.h>

void xor_encrypt_decrypt(char *input, char *key) 
{
    int input_len = strlen(input);
    int key_len = strlen(key);
    for (int i = 0; i < input_len; i++) 
    {
        input[i] = input[i] ^ key[i % key_len];
    }
}

int main() 
{
    printf("***ADVANCED ENCRYPTION STANDARD DES ALGORITHM***\n\n");
    char url[] = "KEERTHIVASAN S";
    char key[] = "secretkey"; 
    printf("Original text: %s\n", url);
    xor_encrypt_decrypt(url, key);
    printf("Encrypted text: %s\n", url);
    xor_encrypt_decrypt(url, key);
    printf("Decrypted text: %s\n", url);
    return 0;
}
```
## OUTPUT:

![ex7op](https://github.com/user-attachments/assets/d45d1e1a-f5aa-422d-b4b0-f9b8605256cb)

## RESULT: 
The program to implement Advanced Encryption Standard DES Algorithm is executed successfully.
