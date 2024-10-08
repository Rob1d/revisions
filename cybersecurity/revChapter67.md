# Revision Sheet for Chapter 6: Basic Mathematics for Cryptography

## Overview
Chapter 6 delves into the mathematical foundations essential for understanding cryptographic systems. Key topics include number theory, primality, GCD, Euler’s Totient Function, Fermat's Little Theorem, and random numbers.

---

## Key Concepts

### 1. **Number Theory Basics**
- **Natural Numbers**: The set of positive integers (1, 2, 3, ...).
- **Integers**: Set of whole numbers (positive, negative, and zero).
  
### 2. **Prime Numbers**
- A prime number is greater than 1 and has no divisors other than 1 and itself.
- **Example**: 2, 3, 5, 7, 11, ...

---

### 3. **Greatest Common Divisor (GCD)**
- The GCD of two integers a and b is the largest positive integer that divides both a and b without leaving a remainder.
  
#### Euclid’s Algorithm:
1. If \( b = 0 \), then \( \text{gcd}(a, b) = a \).
2. Otherwise, \( \text{gcd}(a, b) = \text{gcd}(b, a \mod b) \).

- **Example**: Calculate \( \text{gcd}(54, 30) \)
    1. \( \text{gcd}(54, 30) = \text{gcd}(30, 24) \)
    2. \( \text{gcd}(30, 24) = \text{gcd}(24, 6) \)
    3. \( \text{gcd}(24, 6) = \text{gcd}(6, 0) = 6 \)

---

### 4. **Euler’s Totient Function (φ)**
- Counts the number of integers up to n that are relatively prime to n.
  
**Formula**: 
- For prime \( p \), \( φ(p) = p - 1 \)
- For \( n = pq \) (p and q are primes), \( φ(n) = (p-1)(q-1) \)

- **Example**: 
    - \( φ(10) = 4 \) (1, 3, 7, 9)
    - \( φ(21) = (3-1)(7-1) = 12 \)

---

### 5. **Fermat's Little Theorem**
- States that if \( p \) is a prime and \( a \) is an integer not divisible by \( p \), then:
\[ a^{(p-1)} \equiv 1 \ (\text{mod} \ p) \]

#### Example:
- For \( p = 7 \) and \( a = 3 \):
  - \( 3^{6} \equiv 1 \ (\text{mod} \ 7) \)

---

### 6. **Modular Arithmetic**
- A system of arithmetic for integers where numbers wrap around upon reaching a certain value (the modulus).
  
#### Example:
- \( 12 \mod 5 = 2 \) since 12 divided by 5 leaves a remainder of 2.

---

### 7. **Primitive Roots**
- An integer \( g \) is a primitive root modulo n if every number coprime to n can be expressed as a power of g modulo n.
  
#### Example:
- 2 is a primitive root modulo 5 because 
    - \( 2^1 \mod 5 = 2 \)
    - \( 2^2 \mod 5 = 4 \)
    - \( 2^3 \mod 5 = 3 \)
    - \( 2^4 \mod 5 = 1 \) (covers all numbers 1-4)

---

### 8. **Random Numbers in Cryptography**
- **True Random Number Generators (TRNGs)**: Based on physical phenomena. 
- **Pseudo-Random Number Generators (PRNGs)**: Algorithms that produce number sequences that only approximate true randomness. 

#### Example:
- **Blum, Blum, and Shub (BBS)**: 
    - Uses prime factors \( p \) and \( q \) for generating sequences based on the multiplication modulus.

---

### 9. **Algebraic Structures**
- Cryptography also relies on algebraic structures like groups, rings, and fields, which are essential for operations on integers.

#### Properties of a Group:
1. **Closure**: For any elements a, b in group G, the operation returns another element in G.
2. **Associativity**: For any elements a, b, c in G, \( (a*b)*c = a*(b*c) \).
3. **Identity Element**: There exists an element e in G such that \( a*e = a \).
4. **Inverse Element**: For any a in G, there exists b in G such that \( a*b = e \).

---

## Applications
The mathematical principles discussed are foundational for understanding public key cryptography, algorithms, and security protocols crucial to modern encryption techniques.

---

## Conclusion
Chapter 6 provides essential mathematical knowledge vital for deciphering the complexities of cryptography, focusing on number theory, modular arithmetic, and the structures underpinning many cryptographic algorithms.



# Revision Sheet for Chapter 7: Public Key Cryptography

## Overview
Chapter 7 focuses on public key (asymmetric) cryptography, highlighting the RSA algorithm, the principles behind it, and its applications in secure communications. It also contrasts public key systems with symmetric key systems, discussing their advantages and challenges.

---

## Key Concepts

### 1. **Public Key Cryptography**
- **Definition**: Utilizes two keys - a public key that may be shared and a private key kept secret. This structure allows for secure communication and digital signatures.
  
#### Main Advantages:
1. **Simplified Key Management**: Reduces the need to exchange secret keys as in symmetric systems.
2. **Digital Signatures**: Facilitates the creation of digital signatures for authentication.

---

### 2. **RSA Algorithm**
- One of the most widely used public key cryptosystems.

#### Key Generation:
1. **Choose two large prime numbers**: \( p \) and \( q \).
2. **Calculate \( n \)**: 
   \[
   n = p \times q
   \]
3. **Calculate \( φ(n) \)**: 
   \[
   φ(n) = (p-1)(q-1)
   \]
4. **Choose \( e \)**: An integer such that \( 1 < e < φ(n) \) and \( gcd(e, φ(n)) = 1\).
5. **Determine \( d \)**: The modular multiplicative inverse of \( e \) modulo \( φ(n) \) using the Extended Euclidean algorithm.

#### Key Pair:
- Public key: \( (n, e) \)
- Private key: \( (n, d) \)

#### Encryption/Decryption:
- **Encryption**:
  \[
  c = m^e \mod n
  \]
- **Decryption**:
  \[
  m = c^d \mod n
  \]

#### Example:
- If \( p = 61 \) and \( q = 53 \):
  1. \( n = 61 \times 53 = 3233 \)
  2. \( φ(n) = (61-1)(53-1) = 3120 \)
  3. Choose \( e = 17 \) (which is coprime to 3120)
  4. Calculate \( d \) such that \( ed \mod φ(n) = 1\): \( d = 2753 \)
  
Using these, you can encrypt a message \( m \) as follows:
\[
c = m^e \mod n
\]

---

### 3. **Characteristics of Public Key Cryptographic Systems**
- **Trapdoor Functions**: Easy to compute in one direction but difficult to reverse without a specific piece of information (the private key).
- **Security Assumptions**: Public key systems rely on known hard problems, such as integer factorization and discrete logarithm problems.

### 4. **Applications of Public Key Cryptography**
- **Secure Communication**: Allows for confidential messaging over insecure channels.
- **Digital Signatures**: Ensures the authenticity and integrity of messages.
- **Key Exchange**: Facilitates the secure exchange of session keys.

---

### 5. **Security of RSA**
- Security relies on the difficulty of factoring large integers. As technology advances, key sizes must also increase to maintain security.

#### Recommendations:
- Use at least 2048-bit key lengths for RSA to ensure secure communications.

---

### 6. **Comparison with Symmetric Key Cryptography**
| Feature                        | Public Key Cryptography | Symmetric Key Cryptography |
|--------------------------------|-------------------------|----------------------------|
| Key Type                       | Two keys (public/private)| One shared key             |
| Key Distribution               | Easy (public distribution)| Difficult                   |
| Performance                    | Slower                  | Faster                     |
| Use Case                       | Digital signatures, secure key exchange | Data encryption             |

---

## Conclusion
Chapter 7 illustrates the significance of public key cryptography in modern secure communications, detailing the RSA algorithm's mechanisms and emphasizing its applications and limitations. Understanding these principles is essential for implementing and analyzing secure systems.