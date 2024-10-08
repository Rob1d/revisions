# Revision Sheet for Chapter 4: Theory of Secure Communication

## Overview
This chapter discusses the theoretical underpinnings of secure communication, focusing on models of secure systems, concepts of secrecy, entropy, and the security principles established by Claude Shannon.

---

## Key Concepts

### 1. **Models of Secure Systems**
- **Participants**: Typically comprise **Alice** (the sender) and **Bob** (the receiver), communicating through an insecure channel while being potentially overheard by an attacker, often referred to as **Eve**.
- **Secure Communication**: Achieved through encryption methods that transform plaintext into ciphertext to ensure that any intercepted messages are unintelligible without decryption keys.

#### Example:
- Alice wants to send a message \(M\) to Bob. She encrypts the message using an encryption function \(E(M, K)\), where \(K\) is the key. Bob decrypts the ciphertext \(C\) he receives from Alice using \(D(C, K)\).

### 2. **Shannon’s Theory of Secrecy Systems**
- **Perfect Secrecy**: A system is considered perfectly secure if the probability of the message \(M\) given an intercepted ciphertext \(C\) is equal to the prior probability of the message \(P(M)\) for all messages \(M\). 
- **Entropy**: Measures the uncertainty of a random variable, critical to understanding the effectiveness of a cipher.
  - **Shannon Entropy \(H(X)\)**: Defined for a discrete random variable \(X\) with possible values \(x\) as:
    \[
    H(X) = -\sum P(x_i) \log_2 P(x_i)
    \]
  
### 3. **Equivocation**
- Refers to the uncertainty remaining about the plaintext message after observing the ciphertext. The lower the equivocation, the more information the attacker has about the plaintext.

### 4. **Conditions for Perfect Secrecy**
- **Necessary Conditions**:
  1. \(P(M|C) = P(M)\) for all \(C\) and \(M\): Knowing the ciphertext should not help in guessing the message.
  2. \(P(C|M) = P(C)\) for all \(C\) and \(M\): The distribution of ciphertexts should be independent of the plaintext.

- **Example of Perfect Secrecy**: 
  - **One-Time Pad**: The only known method to achieve perfect secrecy; involves using a random key that is the same length as the message, used only once.
  
### 5. **Random Number Generation**
- **Importance of Randomness**: Essential for key generation in cryptographic systems.
- **True Random vs. Pseudo-Random**: True random number generators (TRNGs) are based on physical phenomena, whereas pseudo-random number generators (PRNGs) use algorithms to produce sequences of numbers that mimic randomness.

### 6. **Complexity Theory**
- Focuses on the computational complexity involved in cryptographic systems. 
  - **Shannon’s Maxim**: “The enemy knows the system” suggests that a cryptographic scheme should remain secure even if the attacker knows the algorithm, relying solely on the secrecy of the key.

---

## Real-World Applications
- **Secure Messaging Protocols**: Secure emails, online banking, and secure communications in applications like Signal or WhatsApp use concepts from Shannon’s theories to protect users' data.
  
### Conclusion
Understanding the theoretical foundations of secure communication equips future professionals with the knowledge to design and analyze secure systems effectively. Claude Shannon's work remains pivotal in guiding modern cryptographic practices.


# Revision Sheet for Chapter 5: Conventional Cryptography Systems

## Overview
This chapter examines conventional cryptographic systems, focusing on symmetric key cryptography, properties of cryptosystems, various cipher classifications, and examples of established algorithms like DES (Data Encryption Standard) and AES (Advanced Encryption Standard).

---

## Key Concepts

### 1. **Conventional Cryptographic Systems**
- **Symmetric Key Cryptography**: Involves a single shared key for both encryption and decryption.
  - **Key Representation**: 
    - \( C = E(K_S, M) \): Encryption
    - \( M = D(K_S, C) \): Decryption
  - Roles of parties:
    - **Alice** (Sender) and **Bob** (Receiver) share a symmetric key \( K_S \).

#### Example:
- Alice sends a secret message to Bob using a shared key. If an eavesdropper (Eve) intercepts the message, she cannot decrypt it without the key.

---

### 2. **Properties of Cryptosystems**
- **Confusion**: Complexity of the relationship between the ciphertext and the key, making it difficult for attackers to derive the key.
- **Diffusion**: The property that ensures small changes in the plaintext result in substantial changes in the ciphertext.

#### Example:
- In encryption algorithms, confusion is achieved through substitution processes (like those in substitution ciphers), while diffusion is accomplished using transposition.

---

### 3. **Classification of Ciphers**
1. **Block Ciphers**:
   - Operates on fixed-size blocks of plaintext (e.g., DES, AES).
2. **Stream Ciphers**:
   - Processes plaintext as a continuous stream of bits or bytes.

#### Example of Block Cipher:
- **DES** (Data Encryption Standard):
  - Input Block Size: 64 bits
  - Key Length: 56 bits
  - Structure: Involves multiple rounds (16 rounds) with substitution and permutation stages.

#### Example of Stream Cipher:
- **RC4**: Fast stream cipher that produces a key stream which is XORed with the plaintext to create ciphertext.

---

### 4. **Detailed Cipher Examples**

#### 4.1 **Substitution Ciphers**
- **Definition**: Every letter in the plaintext is replaced with another letter.
  - **Example**: Caesar Cipher (Shift of 3)
    - Plaintext "HELLO" -> Ciphertext "KHOOR".

#### 4.2 **Transposition Ciphers**
- **Definition**: Rearranging the order of the letters in plaintext according to a defined system.
  - **Example**: Columnar Transposition
    - Plaintext "THIS IS A SECRET MESSAGE" can be arranged in a grid and read in a specific column order.

#### 4.3 **Feistel Cipher**
- **Structure**: The plaintext block is divided into two halves, and a function \( F \) is applied to one half while mixing it with the other.
- **Example**: DES (Data Encryption Standard):
  1. **Initial Permutation (IP)**.
  2. **Feistel Structure**: Each round involves applying the F function, key mixing (XOR), and swapping the halves.

---

### 5. **Standards in Cryptography**
- **DES**: Widely used block cipher previously adopted by NIST.
- **AES**: Currently standard and more secure than DES; supports multiple key sizes (128, 192, 256 bits).

#### Comparison:
| Feature        | DES                    | AES                     |
|----------------|------------------------|-------------------------|
| Key Size       | 56 bits                | 128, 192, 256 bits      |
| Block Size     | 64 bits                | 128 bits                |
| Rounds         | 16                     | 10, 12, 14 (depends on key size) |
| Speed          | Slower due to complexity| Faster due to parallelization |

---

### 6. **Key Management Issues**
- Each user in a large network must manage multiple keys, making key distribution complicated. 
- **Alternative Management**: Use a Key Distribution Center (KDC) where a single shared key between each user and the KDC is used to generate session keys dynamically.

### 7. **Challenges with Conventional Cryptography**
- Although symmetric systems are fast and efficient, key management can become impractical with an increasing number of users due to the quadratic increase in the number of keys needed.

---

## Conclusion
Conventional cryptography relies heavily on the proper management of symmetric keys and provides various tools and techniques for securing information. Understanding these foundational concepts is essential in developing robust security measures for digital communications.