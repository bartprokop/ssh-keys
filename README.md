# SSH Keys

This GitHub repository contains my public SSH keys, currently in use.

## All my SSH keys

| Account    | Key file       | Fingerprint                                                                 |
| ---------- | -------------- | --------------------------------------------------------------------------- |
| bart@e7250 | bart-e7250.pub | 256 SHA256:bJt9eJnLmiZwApHjysqkRWs41Csn8FZ9xvExAKsf4lQ bart@e7250 (ED25519) |
| bart@gcs   | bart-gcs.pub   | 256 SHA256:1y3e7tFhHGf71f7OgVoxT74CbT5GMd52wyw22eQ++QM bart@gcs (ED25519)   |
| bart@paris | bart-paris.pub | 256 SHA256:H9IHKkmJA/nsIBFUBbospEjQrXiV4qGhqDbFcEcbRcg bart@paris (ED25519) |
| bart@t20   | bart-t20.pub   | 256 SHA256:ii8ke6xz2OkiyjDPURqbk+Ar5Y/UvgZ47C9+JwuqDno bart@t20 (ED25519)   |

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

The key's randomart image for `bart@paris` is:

```
+--[ED25519 256]--+
|++o===+o         |
|+.*o+Eo.         |
|oX+B+.o   .      |
|% *ooo . o .     |
|==.o  o S o .    |
|oo  .  . o o     |
|. .       .      |
|                 |
|                 |
+----[SHA256]-----+
```

The key's randomart image for `bart@e7250` is:
```
+--[ED25519 256]--+
|     .....       |
|    +  .. o      |
|  .. +E. o o     |
|....+o..+ .      |
|o= +=..oS        |
|o+O= ooo.+ . o   |
|+*+ . .+o o =    |
|o.      . .= .   |
|         oo.o    |
+----[SHA256]-----+
```

The key's randomart image for `bart@gcs` is:
```
+--[ED25519 256]--+
|                 |
|                 |
|               .o|
|           . +.o=|
|        S . =o%*o|
|         . o EO@=|
|            BoO+B|
|            o* B+|
|           ...=oO|
+----[SHA256]-----+
```
