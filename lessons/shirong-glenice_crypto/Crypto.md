# What is Caesar Cipher?
The Caesar cipher, also known as a shift cipher, is one of the simplest forms of encryption. It is a substitution cipher where each letter in the original message (called the plaintext) is replaced with a letter corresponding to a certain number of letters up or down in the alphabet. (Wikipedia)

It is a simple cipher method and a good way to start learning about encryption.

# What is Substitution Cipher?
An example of Caesar Cipher.
Due to the fast computation logic in today's world, this is usually not used in practice as itself. 
However, an interesting thing to note is that ciphers are just displacements of alphabets, and English words have characteristics. Some alphabets appears more often than the others. (E and T rank highest on the list)
https://en.wikipedia.org/wiki/Letter_frequency 

Hence, to retrieve the original key, we will do frequency analysis of words. 
http://www.counton.org/explorer/codebreaking/frequency-analysis.php

# Cryptanalysis in Python
Using an example from: http://practicalcryptography.com/ciphers/simple-substitution-cipher/ 

We have prepared some easy practices!
This is interesting to try out too: https://cryptopals.com/

# Usage of tools
Online tools are useful in breaking ciphers with English words. However, automation and scripting will definitely be more efficient in CTFs and competitions. 

# Building a script
Let's take a look at this: https://inventwithpython.com/chapter14.html 
Another example can be found at: http://bt3gl.github.io/csaw-ctf-2014-cryptography-200-psifer-school.html 

# Asymmetric Encryption
While symmetric encryption uses only 1 key for encryption and decryption, asymmetric algorithms requires 2 types of keys: Public and Private.

The public key is normally used for **Encryption**.
The private key is normally used for **Decryption**.
*The usage can be reversed and it will yield the same result*. 
The underlying explanation requries a lot of mathematical logic. Because of this, the computational costs are usually high. Most application will use asymmetric cryptography for key distribution and symmetric cryptography for encrpytion/decrpytion.

# Diffie-Hellman
###  An example of Asymmetric Encryption 
Diffie-Hellman is a key agreement protocol, meaning that if two parties (say, the SSL client and the SSL server) run this protocol, they end up with a shared secret K. However, neither client or server gets to choose the value of K; from their points of view, K looks randomly generated. 

It is secret (only them know K; eavesdroppers on the line do not) and shared (they both get the same value K), but not chosen. This is not encryption. A shared secret K is good enough, though, to process terabytes of data with a symmetric encryption algorithm (same K to encrypt on one side and decrypt on the other), and that is what happens in SSL.

*--An explanation found online*
