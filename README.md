# EX.-NO-1-IMPLEMENTATION-OF-CAESAR-CIPHER

## Name: Joshna.M
## Reference Number: 212225230118

# AIM:

To implement the simple substitution technique named Caesar cipher using C language.

# ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

# PROGRAM:
```
#include <stdio.h>
#include <string.h>

int main()
{
    char text[100];
    int key, i;

    printf("Enter plain text: ");
    fgets(text, sizeof(text), stdin);

    printf("Enter key: ");
    scanf("%d", &key);

    key = ((key % 26) + 26) % 26;

    for (i = 0; text[i] != '\0'; i++)
    {
        if (text[i] >= 'A' && text[i] <= 'Z')
            text[i] = (text[i] - 'A' + key) % 26 + 'A';

        else if (text[i] >= 'a' && text[i] <= 'z')
            text[i] = (text[i] - 'a' + key) % 26 + 'a';
    }

    printf("Cipher text: %s", text);

    return 0;
}
```
# OUTPUT:

<img width="1402" height="288" alt="Exp1_Output" src="https://github.com/user-attachments/assets/cb33aa0d-5df2-4e9a-8c9b-48a3c54da9ca" />
