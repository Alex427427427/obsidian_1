Category: [[Information Technology]] [[Information Theory]]
___
### 30000 feet view
A process that takes a message that is about to be transmitted, jumbles it into gibberish (ciphertext) in a specific way before sending. Decryption then unjumbles it at the receiver end. 
### Why?
Why is it necessary to do this? How can naked messages harm you? 
Most services require logging in with a username and password. In the background, these information must be sent over the internet every time you want to login to some service. If this information is naked, eavesdroppers can steal it and login to the services, change your password, and basically rob your account. 
### Keys
Usually requires "keys". Itself a piece of information, a string of bits. 
##### Symmetric Encryption
Both sender and recipient uses the same key. That key is used to encrypt and decrypt messages. 

Fast in operation. 

If the key is stolen, then it's over. 

The key must be shared between the sender and recipient securely. Infinite regress. No true security with only symmetric encryption. 
##### Asymmetric Encryption
More secure. And symmetric encryption still relies on asymmetric encryption to share the common key. 

In asymmetric encryption, sender and receiver each has their own **private key**. That they only store locally. They also each have a **public key** that is openly accessible. 

The public and private keys for a host are linked in very intricate ways, but they cannot be derived from each other. Knowing the public key does not allow for determining the private key. 

**The public key is used for encryption, and the private key is used for decryption**. (only for one specific host)

Example working:
- Both sender S and recipient R has a private and public key. 
- At the start, S and R exchange their public keys. This doesn't need to be secure. 
- S encrypts message with R's public key.
- S sends the message to R. 
- R decrypts the message with R's private key. 
**This is amazing. So the public key gives anyone the power to encrypt messages sent to that host, and yet only the host can decrypt it with their own private key. In some sense the public key (encryption key) is the opposite of the private key (decryption key). So they must be intricately linked, and uniquely identifiable to each other. Yet it is impossible to derive one from the other.** This is only possible due to the utilisation of special mathematical processes. 

For more detailed workings and understanding of how this scheme is possible or helpful, see an example in the [[RSA Algorithm]].

##### Changing Keys
It is safer to change the keys often. This is defined per use case / protocol. 