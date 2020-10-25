# OAUTH

**In the recent past I covered a bit on [Authentication](https://rivad2.github.io/reading-notes/401/class-11.html).


1. **Why is authentication important?**
It is important as it protects valuable data and provides access to only those who are approved by an organization.

1. **Why should we be careful about storing a user’s password?**
Because safety of user data is of utmost importance. Sensitive data is easy to steal if passwords are not properly stored/protected. To properly do this, we have to add multiple layers of security not just one and these encryption, authentication and authorization, hashing and salting.

1. **What is the difference between hashing and encryption?**
Hasing is better than encryption. According to [cybernews.com](https://cybernews.com/security/hashing-vs-encryption/),
>Encryption, when properly executed, forms a kind of invisible vault where data can hide in plain sight. It doesn’t build a wall around the data or lock it away; encryption confounds the data so that casual observers can’t make sense of what they are looking at. This is especially useful if the data consists of personal or classified information, like medical records, credit card information, or trade secrets.

>**Hashing differs significantly from encryption, however, in that it is a one-way process.** There is **no easy way to unscramble the data**, interpret the output, or reverse-engineer the input. There’s no key, no system of two keys, no publicly-accessible keys, no certificates that will grant you access to the original data.


1. **What is the difference between encryption and encoding?:**
The difference here is security as a primary goal. With encoding, security is not a primary goal. Encryption scrambles data to ensure that unintended recipients are not able to make sense out of it is called encryption.


1. **What is a token used for?** A [token](https://en.wikipedia.org/wiki/Access_token#:~:text=A%20token%20is%20used%20to,the%20token%20is%20being%20created.)
A token is used to make security decisions and to store tamper-proof information about some system entity. While a token is generally used to represent only security information, it is capable of holding additional free-form data that can be attached while the token is being created.

### NEW VOCAB TO LEARN:

- **Authentication:**
Authentication is the practice of validating the identity of a registered user attempting to gain access to an application, API, microservices or any other data resource.

- **Authorization:**
Authorization is about deciding whether an individual is permitted to perform a given action on a specific resource once they are authenticated.

- **Encryption:**
The process of converting information or data into a code, especially to prevent unauthorized access.This technique involves a key, which is a set of mathematical values, to turn the data into an encrypted form. The receiver also has the key and uses it to decrypt the data. This process of encryption and decryption is referred to as cryptography.

- **Hashing:**
Hashing is the process of converting a given key into another value. A hash function is used to generate the new value according to a mathematical algorithm. It transforms a string of characters into a value of fixed length. This generated value is called hash.

- **Session:**
A [session](https://en.wikipedia.org/wiki/Session_(computer_science))a session is a temporary and interactive information interchange between two or more communicating devices)

- **Cookie:** A [cookie](https://www.computerscience.gcse.guru/theory/cookies) is a text file stored on a user’s computer by a web browser, at the request of the web server. A cookie is limited to a small amount of data and can only be read by the website that created it.

- **Token:** Ok, there are different types of tokens.  Generally a token is an object (in software or in hardware) which represents the right to perform some operation. There can be client tokens, user tokens, security tokens, payment tokens etc.

- **Basic Auth:** A simple authentication scheme built into the HTTP protocol. The client sends HTTP requests with the Authorization header that contains the word Basic, followed by a space and a base64-encoded(non-encrypted) string username: password.

- **Encoding:** Encoding is done to transform data into a form that can be read by other machines or used by other processes.

- **Secret:** Anything that a developer doesn't want someone else to see. For example, database passcodes, API keys, stuff like that. Anything that could be in an `.env` file for instance.

- **Cryptography:** Cryptography is the study of secure communications techniques that allow only the sender and intended recipient of a message to view its contents. The term is derived from the Greek word *kryptos*, which means hidden.

---------------------
**Resources:**

1.[computerscience.gcse.guru](https://www.computerscience.gcse.guru/theory/cookies)

