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
```
def encrypt(text, key):
    cipher = ""

    for char in text:
        if char.isalpha():
            if char.isupper():
                cipher += chr((ord(char) - ord('A') + key) % 26 + ord('A'))
            else:
                cipher += chr((ord(char) - ord('a') + key) % 26 + ord('a'))
        else:
            cipher += char

    return cipher


def decrypt(cipher, key):
    plain = ""

    for char in cipher:
        if char.isalpha():
            if char.isupper():
                plain += chr((ord(char) - ord('A') - key) % 26 + ord('A'))
            else:
                plain += chr((ord(char) - ord('a') - key) % 26 + ord('a'))
        else:
            plain += char

    return plain


# Main Program
text = input("Enter the plain text: ")
key = int(input("Enter the key value: "))

encrypted = encrypt(text, key)
print("Encrypted Text:", encrypted)

decrypted = decrypt(encrypted, key)
print("Decrypted Text:", decrypted)
```

## OUTPUT:
<img width="1915" height="913" alt="Screenshot 2026-07-22 113434" src="https://github.com/user-attachments/assets/fd8132fc-ed69-4e9c-a09f-3dff3c315bf3" />


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
