# Reading 18 - Cryptography

## Encryption, decryption and cracking

**Caesar Cipher** - invented by Julius Caesar to communicate with his allies.

The cipher is a *substitution* cipher that alternates the original letter and replaces it by *shifting* the alphabet by the desired amount.

*note* Julius Caesar always shifted letters in the cipher by 3.

## Caesar Cipher

mathematical equation of the cipher **encryption**:

En(X) = (X + N) mod 26

**decryption**:

Dn(X) = (X - N) mod 26

**Vigenere Cipher** - shift at each position of text. The value is defined using repeating keywords.

### Breaking the Cipher

**Scenarios**:

1. attacker knows that there is some form of alteration of text using a cipher.

2. Caesar cipher is identified but attack does not know shift value.

Break the cipher by:

1. Completing the plain component; write it out and shift by each number.

2. match frequency distribution of letter (aka **frequent analysis**)

*note* Encrypting text multiple times provides no security

[<==BACK](README.md)
