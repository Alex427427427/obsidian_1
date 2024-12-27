Category: [[Information Technology]]
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

For more detailed workings and understanding of how this scheme is possible or helpful, see an example in the [[RSA Algorithm]].

