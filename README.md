# **Password Encryption & Security Project**

This project implements and analyzes multiple password encryption methodologies as part of the Winter’25 BINF 711 Information Security course. The goal is to compare classical cipher techniques with modern secure password-hashing functions, evaluate their limitations, and demonstrate practical usage in Python using Jupyter Notebook.

---

## 🔐 **Project Overview**

The project is divided into two main requirements:

---

## **1️⃣ Classical Cipher Password Encryption**

We implemented two classical encryption techniques to encrypt stored passwords:

### **✔ Playfair Cipher**
- Generates a 5×5 key matrix  
- Cleans and prepares text into digraphs  
- Handles repeated characters and padding  
- Encrypts and decrypts according to Playfair rules (row, column, rectangle)  
- Fully implemented in Python

### **✔ Vigenère Cipher**
- Implements classical polyalphabetic substitution  
- Supports both encryption and decryption  
- Uses a keyword to shift characters  
- Demonstrates how historical ciphers operate

> **Note:** These classical ciphers are included strictly for academic comparison.  
> They are *not secure* for real-world password storage.

---

## **2️⃣ Modern Password Security Method**

### **✔ PBKDF2 (Password-Based Key Derivation Function 2)**

PBKDF2 was selected as the modern encryption methodology due to:

- Strong industry trust (NIST, OWASP, RFC 8018)
- Uses **salt** to protect against rainbow-table attacks  
- Uses **key stretching** via iterations to slow down brute-force attacks  
- Resistant to basic dictionary attacks  
- Simple to implement and widely available in standard Python libraries  
- Predictable, stable, and well-researched

The implementation includes:
- Random salt generation  
- Secure hashing using PBKDF2-HMAC-SHA256  
- Password verification function  
- Timing analysis to estimate computational cost  
- Clean and modular code written in Jupyter Notebook

---

## 📚 **Research Summary**

The research phase included:
- Evaluating classical ciphers vs. modern password hashing  
- Reviewing security papers and standards on PBKDF2  
- Comparing PBKDF2 with Argon2, bcrypt, and scrypt  
- Understanding the role of **salt**, **iteration count**, and **computational hardness** in password safety  
- Discussing real attack vectors such as brute-force, dictionary attacks, GPU attacks, and rainbow tables

---

## ⚠️ **Limitations**

### **Classical Ciphers (Playfair & Vigenère)**
- Easily broken with modern cryptanalysis  
- Lack salting and key stretching  
- Vulnerable to frequency analysis  
- Provide no resistance to automated attacks  
- Not suitable for secure password storage  

### **PBKDF2**
- More secure than classical ciphers but not memory-hard  
- Attacks using modern GPUs/ASICs can accelerate brute force  
- Must be configured with a sufficiently large iteration count  
- Newer algorithms (Argon2, scrypt) may offer stronger defense in some scenarios  
- Still requires proper parameter tuning by the developer

---

## 🧪 **Testing**

The notebook includes:
- Encryption & decryption tests for Playfair  
- Encryption & decryption tests for Vigenère  
- PBKDF2 hash generation  
- Verification with correct & incorrect passwords  
- Timing analysis for cost measurement  

These tests demonstrate correct functionality and highlight performance considerations.

---

## 🛠 **Technologies Used**
- **Python 3**
- **Jupyter Notebook**
- `hashlib` for PBKDF2
- `os` & `binascii` for salt handling
- `time` for benchmarking

---

## 👤 **Authors**
**Ahmed Hassan**
**Ziad Ekramy**
Faculty of Business Informatics
German University in Cairo    
