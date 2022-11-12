# hashforum
A form of forum in which users are authenticated via usage of a public-private encryption key.

## Introduction

The user can either submit anonymously, in which case they will be given an indexed ID for the post.

### Anonymous authentication

A user will create a 32-digit private key, grouped by twos (base-10) key.

```
86 52 19 43 32 19 87 11 94 25 14 13 67 17 18 54
```

They can securely generate this key and their public key [here](https://searx.org).


The probability that two users would have the same key is $10^{-32}$, this means that if every person on earth were to make two accounts, there would be a $1.6 \times 10^{-23}$ chance (assuming there are 8-billion people on earth).

The user can then edit their profile and info, provided they encrypt a 256 character message with their private key which was assigned to their account earlier. This will allow them to edit their profile for a 10 minute period, before the communication window with the server expires. They must perform the procedure *twice* if they reload, since cookies provide a major security flaw.

The user must regenerate their private and public keys every 30 days for security safety. They can optionally regenerate the keys up to every 5 days. It is reccomended to regenerate your keys every 10 days.
