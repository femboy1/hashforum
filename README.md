# hashforum

A decentralized pseudonymous forum. Users are created and authenticated using an email-less approach.

## Directories

There are two main directories, `host` and `node`.

* `node`: This covers a hashforum server, or an instance of the actual forum service itself.
* `host`: The frontend server. This is a server which makes request to the *node* and then prettifies the results.

## Node interoperability

Users can interact with comments and posts on other nodes using the interop protocol. Posts and comments from other forums will be displayed with a stylistic difference to distinguish between communities.
