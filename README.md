# My SSH keys

This GitHub repository contains my public SSH keys, currently in use.

## All keys

| Account | Key file | Fingerprint |
| ------- | -------- | ----------- |
| bart@t20 | t20-bart-ed25519.pub | 256 SHA256:ii8ke6xz2OkiyjDPURqbk+Ar5Y/UvgZ47C9+JwuqDno bart@t20 (ED25519) |
| bart@xxx | zzzz.pub | no-finger-print-yet |

## Why

I tend to mint new SSH key every time, I install fresh OS from which I want to jump to another box, use git or similar.

## Generation of SSH Key

It is 2022. I will use the `ed25519` algorithm, which is both fast and secure.
Its main strengths are its speed, its constant-time run time (and resistance against side-channel attacks), and its lack of nebulous hard-coded constants.
"Ed25519 is an elliptic curve signature scheme that offers better security than ECDSA and DSA and good performance".

Key generation:

```bash
$ ssh-keygen -t ed25519
```

Fingerprinting SSH key:

```bash
$ ssh-keygen -lf ~/.ssh/id_ed25519.pub
```

Sending the key to remote server:

```bash
$ ssh-copy-id bart@remote-server.org
```

## Keys random art:

The key's randomart image for `bart@t20` is:

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
