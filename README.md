# DSA-Algorithm-
Data Structures &amp; Algorithms (DSA) Implementations of essential data structures and algorithms in multiple languages. Covers arrays, linked lists, trees, graphs, sorting, searching, dynamic programming, and more. Ideal for learning, practicing, and improving problem-solving skills.

---

# Digital Signature Algorithm (DSA) in Java

This project demonstrates the implementation of the **Digital Signature Algorithm (DSA)** in Java for signing and verifying messages. The Digital Signature Algorithm is a cryptographic technique used to ensure the integrity, authenticity, and non-repudiation of data.

### Overview

This project provides a **Java** implementation of the Digital Signature Algorithm (DSA) to:

1. **Generate DSA keys** (public/private key pair).
2. **Sign data** using the private key.
3. **Verify the signature** using the public key.

### Project Structure

The project is divided into three main components:

1. **DSAAlgorithm.java**: Contains logic for generating keys, signing data, and verifying signatures.
2. **Encryptor.java**: Demonstrates how to use the private key to sign data (create a digital signature).
3. **Decryptor.java**: Demonstrates how to use the public key to verify the digital signature of data.

### Prerequisites

Before running the project, ensure you have the following installed:

- **Java 17** or later (Download from [here](https://www.oracle.com/java/technologies/javase-jdk17-downloads.html))
- **Text Editor or IDE** (e.g., IntelliJ IDEA, Eclipse, Visual Studio Code)

### How to Run

#### 1. Generate Keys

To generate the **DSA** key pair (public and private keys), you need to run the `DSAKeyGenerator.java` class. It will create two key files: `privateKey.key` and `publicKey.key`.

Run the following command in your terminal (from the project directory):

```bash
javac DSAKeyGenerator.java
java DSAKeyGenerator
```

The program will generate the keys and save them as **PEM**-encoded files (`privateKey.key` and `publicKey.key`).

#### 2. Encrypt and Sign Data

To **sign** a message (data) using the private key, run the `Encryptor.java` class:

```bash
javac Encryptor.java
java Encryptor
```

This will sign the message `Hello Testing` with the private key (`privateKey.key`), and print the resulting digital signature.

Example output:
```
Generated Digital Signature: MC0CFB8q/YGHiUQDF2284Avb+DnwxvnMAhUAkzQcob8psQ52NMCHFnnotyvPw5U=
```

#### 3. Decrypt and Verify Data

To **verify** the signature, run the `Decryptor.java` class:

```bash
javac Decryptor.java
java Decryptor
```

This will check the validity of the digital signature using the public key (`publicKey.key`), and print whether the signature is valid or not.

Example output:
```
Signature Status: TRUE
Details: The signature matches the data, verifying the authenticity and integrity of the message.
Data Integrity: The data has not been altered, and its authenticity is verified.
Action: Proceed with confidence as the signature is valid.
```

### Notes

- The **DSA** algorithm in this project uses **SHA256withDSA** for signing the data, which ensures the integrity of the message and secures the signature.
- You can modify the data and signatures to test with different messages.
- The project saves keys in **PEM** format for easy storage and retrieval.
- Ensure that the `privateKey.key` and `publicKey.key` files are located in the same directory as the Java program, or modify the paths accordingly.

### License

This project is licensed under the **MIT License**. See the LICENSE file for more details.

---

### Additional Notes:

You can customize the **README** further by adding:

- **Examples of signing and verifying different kinds of data**.
- **A description of the key length** used for DSA (e.g., 2048 bits).
- **References to any additional resources** or articles you used for implementation.
