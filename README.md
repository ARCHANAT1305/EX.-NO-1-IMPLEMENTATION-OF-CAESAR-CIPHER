# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:
### NAME: ARCHANA T
### REGISTER NUMBER: 21222320013
```
#include <stdio.h>

void caesar(char *text, int key) {
    for (int i = 0; text[i]; i++) {
        char c = text[i];
        if (c >= 'A' && c <= 'Z') text[i] = (c - 'A' + key + 26) % 26 + 'A';
        else if (c >= 'a' && c <= 'z') text[i] = (c - 'a' + key + 26) % 26 + 'a';
    }
}

int main() {
    char message[100];
    int key;
    printf("Enter message: ");
    fgets(message, sizeof(message), stdin);
    printf("Enter key: ");
    scanf("%d", &key);

    caesar(message, key);
    printf("Encrypted: %s", message);

    caesar(message, -key);
    printf("Decrypted: %s", message);

    return 0;
}

```

## OUTPUT:


<img width="262" height="170" alt="image" src="https://github.com/user-attachments/assets/a483ac4c-ca65-4ff0-9dfb-19d2414f14f4" />


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
