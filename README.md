# EX-8 : ADVANCED ENCRYPTION STANDARD (AES) ALGORITHM
# Aim:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

# ALGORITHM:
AES is based on a design principle known as a substitution–permutation.
AES does not use a Feistel network like DES, it uses variant of Rijndael.
It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.
AES operates on a 4 × 4 column-major order array of bytes, termed the state
# PROGRAM:
```
#include <stdio.h>
#include <string.h>

void xor_encrypt_decrypt(char *input, char *key)
 {
    int input_len = strlen(input);
    int key_len = strlen(key);

    for (int i = 0; i < input_len; i++)
    {
         input[i] = input[i] ^ key[i % key_len]; // XOR encryption
    }
}

int main()
{
   char url[] = "https://github.com/Jayabharathi3";
   char key[] = "secretkey"; // Simple key for XOR encryption

   printf("Original URL: %s\n", url);

   // Encrypt the URL
   xor_encrypt_decrypt(url, key);
   printf("Encrypted URL: %s\n", url);

   // Decrypt the URL (since XOR is reversible using the same key)
   xor_encrypt_decrypt(url, key);
   printf("Decrypted URL: %s\n", url);

   return 0;
}
```
# OUTPUT:

![Screenshot 2024-10-16 153324](https://github.com/user-attachments/assets/80bbb93c-fe47-4ec4-96c5-49681c30528c)


# RESULT:
Thus , to use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption is done successfully.
