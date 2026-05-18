# Cryptography --- 19CS412 - Advanced Encryption Standard DES Algorithm

# EXP - 7 ADVANCED ENCRYPTION STANDARD DES ALGORITHM

## AIM:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

## ALGORITHM: 

STEP-1: Start the program and include the required header files.

STEP-2: Read the plaintext input and encryption key from the user.

STEP-3: Calculate the length of the text and key using strlen().

STEP-4: Perform XOR operation between each character of the plaintext and key to generate encrypted text.

STEP-5: Apply the same XOR operation again using the same key to decrypt the encrypted text.

STEP-6: Display both encrypted and decrypted outputs, then end the program.

## PROGRAM: 

```
#include <stdio.h>
#include <string.h>

void xorEncryptDecrypt(char text[], char key[], int len)
{
    int i;
    int keyLen = strlen(key);
    for(i = 0; i < len; i++)
    {
        text[i] = text[i] ^ key[i % keyLen];
    }
}

void printEncrypted(unsigned char text[], int len)
{
    int i;
    for(i = 0; i < len; i++)
    {
        printf("%02X ", text[i]);
    }
    printf("\n");
}

int main()
{
    char text[100];
    char key[] = "SECRET";
    int len;
    printf("XOR ENCRYPTION AND DECRYPTION\n\n");
    printf("Enter Text : ");
    fgets(text, sizeof(text), stdin);
    text[strcspn(text, "\n")] = '\0';
    len = strlen(text);
    printf("\nOriginal Text  : %s\n", text);
    xorEncryptDecrypt(text, key, len);
    printf("\nEncrypted Text : ");
    printEncrypted((unsigned char *)text, len);
    xorEncryptDecrypt(text, key, len);
    printf("Decrypted Text : %s\n", text);
    return 0;
}
```
## OUTPUT:

<img width="1916" height="905" alt="ex7op" src="https://github.com/user-attachments/assets/1d2f970a-bb6c-4d8b-9ee7-efb7cd9e1512" />

## RESULT: 
Thus, the implementation of DES Encryption and Decryption had been executed successfully.
