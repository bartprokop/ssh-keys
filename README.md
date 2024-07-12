# My SSH Keys

This GitHub repository contains my public SSH keys, currently in use.

## All my SSH keys

| Account    | Key file       | Fingerprint                                                                 |
| ---------- | -------------- | --------------------------------------------------------------------------- |
| bart@e7250 | bart-e7250.pub | 256 SHA256:bJt9eJnLmiZwApHjysqkRWs41Csn8FZ9xvExAKsf4lQ bart@e7250 (ED25519) |
| bart@gcs   | bart-gcs.pub   | 256 SHA256:1y3e7tFhHGf71f7OgVoxT74CbT5GMd52wyw22eQ++QM bart@gcs (ED25519)   |
| bart@paris | bart-paris.pub | 256 SHA256:dreFMQBoUhsBq+y9Q/CV/RLM1p2zeun0FvsZsO9xh5U bart@paris (ED25519) |
| bart@t20   | bart-t20.pub   | 256 SHA256:ii8ke6xz2OkiyjDPURqbk+Ar5Y/UvgZ47C9+JwuqDno bart@t20 (ED25519)   |


## Verification of this repository

You can use `git` command to verify cryptographically content of this repository.
First you must import keys, I've used - over the years to sign commits.

```bash
$ curl https://prokop.dev/.well-known/openpgpkey/fp/8B06BE97D20CDCB9C3919FDC03E27335904EEBF4.asc -s | gpg --import
gpg: key 03E27335904EEBF4: 1 signature not checked due to a missing key
gpg: /home/bart/.gnupg/trustdb.gpg: trustdb created
gpg: key 03E27335904EEBF4: public key "Bart Prokop (git signing key 20180908) <prokop.bart@gmail.com>" imported
gpg: Total number processed: 1
gpg:               imported: 1
gpg: no ultimately trusted keys found
```

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
