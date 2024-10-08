# Revision Sheet for Chapter 1: Introduction to Information Security

## Course Information
- **Instructor**: David (Bong Jun) Choi
- **Institution**: Computer Science and Engineering, Soongsil University
- **Contact**: davidchoi@soongsil.ac.kr

---

## Course Description
This course provides an in-depth understanding of various principles and practices in computer security, specifically focusing on:
- Cryptography
- Cryptanalysis
- Public Key Infrastructure (PKI)
- Application and Transport Layer Security Protocols
- Network Attacks and Defense Mechanisms

### Prerequisites
- Discrete Mathematics
- Computer Networks
- Probability and Statistics

---

## Course Outline
### Key Topics Covered:
1. Introduction to Information Security
2. Basic Concepts and Security Requirements
3. History of Cryptography
4. Network and Systems Under Attack
5. Theory of Secure Communication
6. Models of Secure Systems
7. Conventional (Symmetric Key) Cryptography Systems
8. Basic Mathematics for Cryptography
9. Public Key Cryptography
10. Advanced Cryptographic Techniques
11. Privacy-Preserving Protocols

---

## Course Objectives
By the end of this course, students will be able to:
1. Understand principles and practices in information security.
2. Identify threats, vulnerabilities, and countermeasures of various systems.
3. Implement secure information systems effectively.

---

## Key Concepts
### Information Security Definitions
- **Confidentiality**: Ensures that information is not disclosed to unauthorized entities.
- **Integrity**: Assurance that information remains accurate and unaltered.
- **Availability**: Guarantee that information and resources are accessible when required.

### Threats in Information Security
- Exposure of sensitive information
- Data tampering
- Identity impersonation
- Service disruption
- Unauthorized access to information systems

---

## Important Resources
### Recommended Textbooks:
- William Stallings, “Cryptography and Network Security: Principles and Practice”
- Bruce Schneier, “Applied Cryptography: Protocols, Algorithms, and Source Code in C”

### Grading Policy
- **Attendance**: 10%
- **Assignments**: 10%
- **Quizzes**: 10%
- **Midterm Exam**: 30%
- **Final Exam**: 40%

*Note: All assignments must be submitted in English and can incur penalties for late submissions.*

---

## Summary
Chapter 1 serves as an introduction to the vast field of information security, laying the groundwork for the concepts of confidentiality, integrity, availability, and various security mechanisms. The outlined structure of the course helps give an understanding of both theoretical and practical aspects of securing information systems.

---


# Chapter 2

# Revision Sheet for Chapter 2: History of Cryptography

## Key Concepts

### 1. Early Cryptographic Techniques
- **Scytale (Transposition Cipher)**: Used by the Greeks; involved wrapping a message around a rod to reveal it.
- **Code Book (Substitution Cipher)**: Replaced letters with numbers (e.g., A=1, B=2).
- **Caesar Cipher**: A transposition method where each letter was shifted n places, popularized by Julius Caesar (e.g., shifting by 3).

### 2. The Enigma Machine
- Employed by the Germans during WWII for secure communication.
- Featured rotors and a plugboard; configurations were changed daily, creating a vast keyspace.

### 3. Mathematical Foundations
- **Claude E. Shannon**: Published "A Mathematical Theory of Cryptography" in 1949; introduced key concepts of secrecy and unicity distance.
- **Data Encryption Standard (DES)**: Established in 1975 to ensure secure communication for businesses.

### 4. Modern Advances
- **Diffie-Hellman Key Exchange**: Introduced asymmetric cryptography and the ability to securely exchange cryptographic keys over a public medium.

### 5. Future Trends
- **Emerging Security Issues**:
  - Importance of security for networked devices due to increasing data flows.
  - Challenges posed by cloud computing, mobile devices, and quantum computing.

---

## Case Studies

### Case Study 1: Sending a Diamond Ring
- Alice sends an empty box to Bob; Bob locks and returns it with the diamond, after which Alice opens it.

### Case Study 2: Russian Postal System Puzzle Key Exchange
- Involves locking mechanisms where Alice and Bob independently add their locks to exchange valuables securely.

---

## Cryptographic Objectives
- **Confidentiality**: Keeping information secret from unauthorized access.
- **Integrity**: Ensuring data is not altered in transit.
- **Authentication**: Verifying identities of parties involved in communication.
- **Non-repudiation**: Preventing denial of sending messages.
- **Availability**: Ensuring that systems are operational when needed.

---

## Conclusion
The study of cryptography has evolved significantly, from ancient techniques to modern systems like the Enigma, DES, and contemporary key exchange methods. As digital communication grows, so does the need for effective security measures to protect sensitive information against emerging threats.

# Revision Sheet for Chapter 3: Cryptographic Tools

## Overview
This chapter focuses on the various cryptographic tools that play a pivotal role in ensuring confidentiality, integrity, authentication, and other security objectives in information security.

---

## Key Cryptographic Tools

### 1. **Encryption/Decryption**
- **Encryption**: The process of transforming plaintext into ciphertext using an encryption algorithm and a key.
  - **Formula**: \( C = E(M, K) \)
- **Decryption**: The reverse process of encryption that converts ciphertext back into plaintext using a corresponding key.
  - **Formula**: \( M = D(C, K) \)

#### Types of Cryptography:
- **Symmetric Key Cryptography**:
  - Same key used for both encryption and decryption (e.g., AES, DES).
  - **Example**: If the key is shared between two parties, data can be encrypted and decrypted affordably.
  
- **Asymmetric Key Cryptography**:
  - Different keys are used for encryption (public key) and decryption (private key).
  - **Example**: RSA (Rivest–Shamir–Adleman) is widely used for secure data transmission; the public key is available for anyone to use, while the private key is kept secret by the owner.

---

### 2. **Message Authentication Code (Hashing)**
- Hashing ensures data integrity by producing a fixed-size output (hash) from variable-size input data.
- **Requirements for Cryptographic Hash Functions**:
  1. **Easy Computation**: It must be simple to compute a hash for any input.
  2. **Preimage Resistance**: It should be infeasible to revert the hash output back to the original input.
  3. **Collision Resistance**: Two different inputs should not produce the same hash output.
  
- **Common Hash Functions**:
  - SHA-256 (Secure Hash Algorithm)
  - MD5 (not recommended due to vulnerabilities)

**Real-World Example**: Hashing can be used to maintain the integrity of files; if a file is modified, its hash will change, alerting the user to a potential attack.

---

### 3. **Digital Signatures**
- A method to verify the authenticity and integrity of a message.
- Involves using a private key to sign a document and a public key for verification.
  
#### Steps:
1. **Signing**: The sender creates a hash of the message and encrypts it with their private key.
2. **Verification**: The recipient decrypts the hash with the sender's public key and compares it with the hash generated from the received message.
  
### Example Use Case:
- In financial transactions, digital signatures ensure that messages (like payment instructions) are authentic and have not been altered in transit.

---

### 4. **Randomness**
- Essential for generating cryptographic keys and ensuring secure communications.
- Modern systems use **Cryptographically Secure Pseudo Random Number Generators (CSPRNG)** to create unpredictable values.
  
#### Importance of Randomness:
- The security of any encryption system can be compromised if the keys are predictable; high-quality randomness is crucial.

---

## Security Principles
- **Kerckhoffs's Principle**: The security of cryptographic systems should rely on the secrecy of the key only, not the algorithm.
- **Availability**: Ensuring that authorized users have access when needed; involves backup and redundancy strategies.

---

## Summary
Cryptographic tools are vital in safeguarding digital communications and data. Understanding how encryption, hashing, digital signatures, and randomness work provides the foundation for implementing secure information systems. 

---


