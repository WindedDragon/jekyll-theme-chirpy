---
layout: post
title:  "gpg Basics"
date:   2019-01-21 22:07:01 -0600

categories: gpg encryption mutt email
---

### Creating and Decrypting files for safely storing pws

##### Mutt example

Create a password file.`~/.mutt/passwords`:

```
set imap_pass="password"
set smtp_pass="password"
```

To encrypt using GPG a keypair is needed first:

```bash
gpg --gen-key
```

Encrypt the file:

```bash
$ gpg -r *your.email@example.com* -e ~/.mutt/passwords
$ shred ~/.mutt/passwords
$ rm ~/.mutt/passwords
```

Add to `muttrc` :

```bash
source " gpg -d ~/.mutt/passwords.gpg |"
```

```bash
source " gpg2 -q --for-your-eyes-only --no-tty -d ~/.config/mutt/passwords.gpg |"
```
