## 7 Cryptography Concepts ever developer must know 🔐

This README provides a clear, high-level overview of seven core cryptographic concepts. It focuses on definitions, properties, and real-world use cases and code.
## Have Fun: 
Use the code, test and manually compare with the methods you learnt from school.
Watch the video to have a good explanation or review.

Table of Contents

# Hash Function
# Salting
# HMAC
# Symmetric Encryption
# Keypairs
# Digital Signature
# Asymmetric Encryption
# Interplay of Concepts
# Source

# 1. Hashing

A hash function takes an input (or "message") and returns a fixed-size string of bytes. The output, called a digest, is unique for different inputs with a very high probability.

• Properties:

• Deterministic: Same input always produces the same digest.

• One-way: Cannot feasibly invert the digest to recover original data.

• Collision-resistant: Hard to find two distinct inputs that produce the same digest.

• Use Cases:

• Storing passwords securely (store the digest, not the password).

• Verifying file integrity (checksums).

• Deduplication of data in storage systems.

<!-- Run the code -->
# node Hash

# 2. Salting

A salt is a random value added to input data before hashing. Salting prevents attackers from using precomputed tables (rainbow tables) to reverse common hashes.

• Properties:

• Unique per user/password.

• Stored alongside the hash.

• Increases entropy and ensures distinct hashes for identical inputs.

• Use Cases:

• Password storage in databases.

• Enhancing key derivation processes for user credentials.

<!-- Run the code -->
# node Salting

# 3. HMAC (Hash-based Message Authentication Code)

An HMAC combines a secret key with the message data and processes it through a hash function to produce a secure code that verifies both the integrity and authenticity of the message.

• Properties:

• Requires a shared secret key.

• Resistant to length extension attacks (depending on the underlying hash).

• Provides both integrity and authenticity.

• Use Cases:

• API request signing.

• Secure cookie generation/validation.

• Verifying messages in distributed systems.

<!-- Run the code -->
# node HMAC

# 4. Symmetric Encryption

Symmetric encryption uses the same secret key to both encrypt plaintext and decrypt ciphertext.

• Properties:

• Fast and efficient for bulk data.

• Key distribution is a challenge—both parties must securely share the same key.

• Use Cases:

• Encrypting files at rest (e.g., disk encryption).

• Securing network traffic in VPNs and TLS sessions.

• Database field encryption.

<!-- Run the code -->
# node SymEncrypt

# 5. Key Pairs

In asymmetric cryptography, a key pair consists of a private key (kept secret) and a public key (shared openly).

• Properties:

• Public key encrypts or verifies signatures.

• Private key decrypts or creates signatures.

• Generated together and mathematically linked.

• Use Cases:

• Secure key exchange mechanisms.

• Identity verification.

• Establishing trust in certificate-based systems.

<!-- Run the code -->
# node Keypair

# 6. Asymmetric Encryption

Asymmetric encryption leverages a recipient’s public key for encryption and the corresponding private key for decryption.

• Properties:

• Eliminates need for a shared secret channel.

• Computationally more intensive than symmetric encryption.

• Use Cases:

• Secure email (PGP/GPG).

• HTTPS/TLS handshake for negotiating session keys.

• Encrypting small messages or session keys.

<!-- Run the code -->
# node AsymEncrypt

# 7. Digital Signature

A digital signature is created by hashing a message and then encrypting the digest with the sender’s private key. Recipients verify the signature using the sender’s public key.

• Properties:

• Authenticity: Confirms the message came from the claimed sender.

• Integrity: Detects any alteration of the message.

• Non-repudiation: Sender cannot deny signing.

• Use Cases:

• Code signing for software distribution.

• Signing legal documents electronically.

• Transaction validation in blockchain systems.

<!-- Run the code -->
# node DigSign

# 8. Interplay of Concepts

• User Authentication: Salt + hash passwords; optionally wrap with HMAC.

• Secure Channels: Use asymmetric encryption for key exchange, then symmetric encryption for bulk data.

• Data Integrity & Authenticity: Apply HMACs for shared-key environments; use digital signatures in public-key contexts.

# 9. Source

• Fireship.io Cryptography Video: [https://www.youtube.com/watch?v=NmM9HA2MQGI](https://youtu.be/NuyzuNBFWxQ?si=AbtuvdjpuwMGOtxy)



