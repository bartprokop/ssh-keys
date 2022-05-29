# My SSH keys

## Bart Prokop SSH public keys

This repository contains my public SSH keys, currently in use.

I tend to mint new SSH key every time, I install fresh OS from which I want to jump to another box, use git or similar.

## Generation of SSH Key

It is 2022. We will use the `ed25519` algorithm, which is both fast and secure.
Its main strengths are its speed, its constant-time run time (and resistance against side-channel attacks), and its lack of nebulous hard-coded constants.
"Ed25519 is an elliptic curve signature scheme that offers better security than ECDSA and DSA and good performance".

```bash
$ ssh-keygen -t ed25519
```

## List of my public keys

## Keys random art:

bart@t20

The key fingerprint is:
SHA256:ii8ke6xz2OkiyjDPURqbk+Ar5Y/UvgZ47C9+JwuqDno bart@t20

The key's randomart image is:
```
+--[ED25519 256]--+
|                 |
|                 |
|                 |
|                 |
|.o. .   S        |
|o.*O.. .         |
|+*XOo..          |
|B*E*@..          |
|XB*&B*.          |
+----[SHA256]-----+
```
