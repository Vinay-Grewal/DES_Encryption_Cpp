# DES_Encryption_Cpp
This C++ program implements DES encryption for a 64-bit plaintext and 64-bit key, both given in hexadecimal.

This project implements the Data Encryption Standard (DES) algorithm in C++ to securely encrypt 64-bit plaintext blocks using a 64-bit key, both provided as 16-character hexadecimal strings. The implementation follows the classical DES procedure including initial permutation, 16 Feistel rounds with key-based substitution and permutation, and final permutation to produce the ciphertext.

Key Features and Functions:

1. encrypt(plain_txt, key)
The primary function executing the DES algorithm. It generates 16 sub-keys through permutations and left shifts, performs the initial permutation on the plaintext, applies 16 rounds of encryption with expansion, substitution (via S-boxes), permutation, and XOR operations, and finally executes the inverse permutation to produce the encrypted output.

Key Scheduling Functions:

2. shift_bit: Performs circular left shifts on key halves for sub-key generation.

3. xor_add: Executes bitwise XOR between binary strings.

4. get_element_from_box: Applies S-box substitution to transform 6-bit inputs into 4-bit outputs.

Utility Functions:

5. Hex_to_Bin and Bin_to_Hex convert data between hexadecimal and binary formats.

6. Dec_to_Bin converts decimal values to fixed-length binary strings.

Object-Oriented Design:

The entire encryption process is encapsulated within the DES_Encryption class, which manages the encryption logic, key scheduling, and utility conversions internally.

Private members store constants such as permutation tables and S-boxes, safeguarding them from external access.

A clean public interface exposes the encrypt method for ease of use.

This modular design promotes code reuse and maintainability, allowing future enhancements like decryption or alternative key management.
