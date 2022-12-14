# hashforum

A decentralized pseudonymous forum. Users are created and authenticated using an email-less approach.

## Node interoperability

Users can interact with comments and posts on other nodes using the interop protocol. Posts and comments from other forums will be displayed with a stylistic difference to distinguish between communities.

## Getting started

Running a hashforum instance is an exciting venture, allowing you to personally host, control, and customize your own forum.

### Prerequisites

* Node.js runtime (>=18.0.0)
* `npm` and `yarn`
* A valid C & C++ compiler, able to compile C++17.

### Bootstrapping

Upon downloading the latest hashforum-node source, unzip it and extract it to a chosen directory. Then run `yarn install` to install all the dependencies.

### First-time execution

A large portion of important files are un-made on a first-time execution and will be created.

```bash
# Start a single-thread server and then shutdown after startup (creates the files)
./node start --jobs=1  --verbose --no-serve
```

You can the edit the config files and start up.

## File security

Upon start, you may have noticed the `(security) File <> validated!` message. This occurs simply because there is a hidden `.files-checksum` file which stores the checksum of all internal files (those not for user modification). If the checksums don't match, it will attempt to recover the system before starting. You can easily bypass this check by either silencing these errors (`--no-security`) or running a rehash (`./node rehash --changed-only`).
