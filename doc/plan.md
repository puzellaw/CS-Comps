# Implementation of AES
Our Group REPO where all work is currently being done: __https://github.com/puzellaw/AES.git__
## Description 
The Advanced Encyption Standard or AES is a cryptographic algorithm used in many security systems today. AES is a varient of the Rjyndael block cipher that won the NIST competition for the next encyption standard<sup>1</sup>. This crptographic hash function takes a 128, 192, or 256 bit key that is used to encrypt and decrypt input files. Depending on the key size will execute the encyption algorithm for 10, 12, or 14 rounds respectively. 

## Goals
- Understand the internal structure of the working of AES (why does it execute the functions it uses in the order it uses them).
- Understand common attacks for AES and where implementation vulnerabilites are common.
- Understand in-depth how each function works: SubBytes, ShiftRows, MixColumns, and AddRoundKey.
- Lean as much as we can about other aspects of AES.

## Development Goals
- Implement all functions as defined by implementation standard<sup>2</sup>
    - `ADDROUNDKEY()`
    - `AES-128()`
    - `AES-192()`
    - `AES-256()`
    - `CIPHER()`
    - `EQINVCIPHER()`
    - `INVCIPHER()`
    - `INVMIXCOLUMNS()`
    - `INVSBOX()`
    - `INVSHIFTROWS()`
    - `INVSUBBYTES()`
    - `KEYEXPANSION()`
    - `KEYEXPANSIONEIC()`
    - `MIXCOLUMNS()`
    - `ROTWORD()`
    - `SBOX()`
    - `SHIFTROWS()`
    - `SUBWORD()`
    - `XTIMES()`
- Implement a basic 128, 192, and 256 bit AES algorithm.

- Implement AES with CBC (Cipher Block Chaining).

- (Stretch) Implement AES with other Block Cipher modes

- (Stretch) Compare efficiency with openSSL's AES implementation.

- (Stretch) Add support for multiple 

# Architecture
We are planning on making our project a C program that takes command line arguments and does everything in the terminal.

# Testing and Benchmarks
For testing and benchmarking we will use test cases provided by the NIST specification document along with comparisions against openSSL's implementation of AES. We plan to compare our final implementation of AES against multiple market implementations that we will investigate. 

# Development Schedule
- Week 3 - Create Framework and test suite. Begin implementing `ADDROUNDKEY()`
- Week 4 - Finish implementing `ADDROUNDKEY()` and `SBOX()`
- Week 5 - Finish implementing `SHIFTROWS()` and `MIXCOLUMNS()`
- Week 6 - Finish implementing AES128, AES192, AES256 and start working on inverse functions
- Week 7 - Finish inverse cipher
- Week 8 - Test
- Week 9 - Implement Stretch Goals
- Week 10 - Present

# Prelimiary Implementation Issues
Our reading of the algorithm implementation documentation has left us with a few preliminary areas that we beleive will be difficult to implement. Orriginally we thought that `AddRoundKey()` would have been an issue for implementation but we have since implemented it with testing. As we continue to implement the forward functions we beleive that we may struggle implementing the reverse Key Expansion funtion. 


# Communication & Working together
We plan to meet three times a week outside of class to make sure that the two of us are on track. We plan to divide the work up by splitting up our implementation each week at the beggining of the week. As we each have our strengths we will try to cater to those as possible to make the project as easy as possible. We will keep eachother accountable by maintaining constant communication of both our commitments inside and outside of class to make sure that work is being completed in a timely manner. 
# Sources

1. https://en.wikipedia.org/wiki/Advanced_Encryption_Standard
2. https://www.nist.gov/publications/advanced-encryption-standard-aes
