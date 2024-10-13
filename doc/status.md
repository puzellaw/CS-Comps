# Status Update

## Implementation So Far
So far we have implemented AES encryption for all block sizes. This implementation of AES encryption includes an implementation of the following functions:
- `AddRoundKey()`
- `AES_128()`
- `AES_192()`
- `AES_256()`
- `Cipher()`
- `keyExpansion()`
- `RotWord()`
- `MixColumns()`
- `SBox()`
- `ShiftRows()`
- `SubWord()`
- `XTimes()`
Functions implemnted for Decryption:
- `invMixColumns()`
- `invShiftRows()`
- `invSubBytes()`
We have also finished all decryption functions aside from Inverse Key Expansion and InverseCi

## Currently implenting. 

We are currently implementing InverseKeyExpansion and InverseCipher, though this will be difficult without finding a inverse key schedule to compare to. Once we have implemented these functions we will being working on packaging our implementation to make it usable in the terminal and to start working on cipher block modes. We are also continuing to build out our testing suite.