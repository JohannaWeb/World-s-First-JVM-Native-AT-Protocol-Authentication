# AT Protocol JVM Auth Filter

The world's first native JVM implementation of **atproto** authentication, supporting **ES256K** and **DPoP**.

## The Achievement
This project was developed "for fun" to solve the lack of native Java support for AT Protocol identity. It was successfully demoed at **UPTEC (Porto)** to prove that sovereign identity can run high-performance on the JVM without Node.js wrappers.

## Technical Highlights
* **Native ES256K:** Manual implementation of `secp256k1` signature verification using Bouncy Castle primitives.
* **Low-S Normalization:** Built-in protection against signature malleability (a common failure point in JVM crypto).
* **Multicodec Handling:** Native decoding of `publicKeyMultibase` prefixes.
* **Identity Bridging:** Seamlessly maps `did:web` and HTTPS PDS issuers.

##  Stack
* **Java 25**
* **Spring Boot 4.x**
* **Bouncy Castle Primitives**

https://gist.github.com/JohannaWeb/81e304f13c9264ae5ae8bc38b79a1141
