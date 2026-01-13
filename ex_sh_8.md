# Ex. 1 - DOs and DON’Ts of Code and Connections

## a) Secure connections should be encrypted, authenticated and tamper-proof. Explain why and how this is achieved.

We need secure conections because when dealing with sensitive data we need to have everyone authenticated with no other third party being able to read or alter the messages.

## b) Name some problems that can occur when sanitizing data.

 We might forget to sanitize data.
 Data might be sanitized the wrong way

## c) Why is sanitization of debug / logging output important as well?

To anonimize users and not leak user data. If the data is stored in a not so secure server that could lead to direct harm to users or the company if it gest leaked.

# Ex. 2 - Cryptography

## a) Explain how a symmetric encryption works.

Both parties have the same cryptographic key.

## b) Explain how an asymmetric encryption works.

One party has a private key, that can be used to sign or to decrypt a message.

Another has a public key, that can be used to verify a signature of to encrypt a message.

## c) Compare stream cipher with block ciphers.

Stream cypher the key is turned into a key and the plaintext is converted to ciphertext by xor-ing with the key.

Block cipher the message is split into to blocks and each block is encripted, can be paralelized, but corelations can be made with the encripted blocks.

# Ex. 3 - Message Authentication Codes (MAC) and Signatures

[//]: # (Change the order of the questions)


[//]: # (Not really specified in the slides)
## a) What are MACs used for and how do they work?

MACs are a guarantee that a given sendere wrote a message, there will be a code that can be used by the reciever to validade the message using a specific algorithm and key.

The most secure way to is to encript a message and then run it through the MAC algorithm to ensure that both the ciphertext and the original text are intact.

[//]: # (Not really specified in the slides)
## b) What are signatures used for and how do they work?

Signatures are used to prove that a given entity has writen a given artifact. I works by hashing the artifact and then encripting that hash, it can then be sent with the arifact so that any one with the decription key can see that the artifact was not altered.

[//]: # (Are they both for the same pourpose?)
# Ex. 4 - RTFM

In the lecture, two papers were cited on why no one reads the manual. Answer the following sub-tasks:

## a) What are common alternatives to reading the manual that users used?

Look it up on google, a llm, or forum.

## b) Why were manuals not used?

Hard to read, or not made for the target audience.

## c) What makes a good manual?

Short, with good examples.

# Ex. 5 - Vulnerability of the Day - Hard-coded credentials and unsalted hashes