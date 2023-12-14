# Caesar Cipher Decryption Tool

## Overview
This repository contains a Python script for decrypting messages encoded using the Caesar cipher. The Caesar cipher is a simple substitution cipher where each letter in the plaintext is shifted a certain number of places down or up the alphabet.

## How it Works
The script `caesar_cipher_decrypt.py` includes a function `caesar_cipher_decrypt` which takes a ciphertext (the encrypted message) and a shift value as inputs. It returns the decrypted plaintext. The function checks if each character is a letter and applies the shift accordingly, wrapping around the alphabet where necessary.

## Usage
1- Clone or download this repository to your local machine.
2- Run the script caesar_cipher_decrypt.py.
3- Enter the ciphertext and the shift value when prompted.
4- The script will output the decrypted plaintext.

## Contributing
Contributions to this project are welcome. Please fork the repository and submit a pull request with your changes.

## Code Snippet
```python
def caesar_cipher_decrypt(ciphertext, shift):
    decrypted = ""
    for char in ciphertext:
        if char.isalpha():  # Check if the character is an alphabet
            shifted = ord(char) - shift
            if char.islower():
                if shifted < ord('a'):
                    shifted += 26
            elif char.isupper():
                if shifted < ord('A'):
                    shifted += 26
            decrypted += chr(shifted)
        else:
            decrypted += char
    return decrypted

