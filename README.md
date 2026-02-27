# 🔐 PYGEN
### Advanced Password Generator & Entropy-Based Strength Checker

> **PYGEN** is a professional command-line password utility written in Python.
It generates **cryptographically secure passwords** and evaluates password strength using **real entropy calculation**, not fake “weak / medium / strong” rules.

---

## ✨ Why PYGEN?

Most password tools:
- Guess strength using rules ❌
- Depend only on password length ❌

**PYGEN uses real mathematics.**  
It calculates password strength using **entropy**, the same concept used in cybersecurity and cryptography.

---

## 🚀 Features

✔ Secure Random Password Generator  
✔ Entropy-Based Strength Checker (bits)  
✔ Clear Strength Classification  
✔ Clean & Minimal CLI Interface  
✔ ANSI Color Output  
✔ Single-File Architecture  
✔ Cross-Platform (Linux / Windows / macOS)

---

## 🧠 How Password Strength Is Calculated

PYGEN uses the entropy formula:

```

Entropy = log₂(N^L)

````

Where:
- **N** = size of the character set  
- **L** = password length  

Higher entropy means **stronger resistance against brute-force attacks**.

---

## 📸 Preview

![PYGEN Screenshot](https://github.com/user-attachments/assets/db308385-e7d2-4116-a63b-88f757bb8d16)

---

## 📦 Installation

Clone the repository:

```bash
git clone https://github.com/AntorDOS/PyGen.git
cd PyGen
````

Run the tool:

```bash
python3 pygen.py
# or
./pygen.py
```

No external dependencies required.

---

## 🛠 Usage

* Generate strong random passwords
* Check entropy of existing passwords
* Understand how character sets affect strength

Ideal for:

* Cybersecurity learners
* Ethical hacking practice
* Developers & system administrators
* Password policy testing

---

## 🔐 Use Cases

* Penetration testing labs
* Security awareness training
* CLI-based security tools
* Learning entropy & brute-force resistance

---

## 📁 Project Structure

```
PyGen/
 ├── pygen.py      # Main program
 └── README.md     # Documentation
```

Simple, clean, and easy to audit.

---

## ⚠️ Disclaimer

This tool is intended for **educational and defensive purposes only**.
The author is not responsible for any misuse.

---

## 👤 Author

**Md Jahid Hasan Antor**
GitHub: [https://github.com/AntorDOS](https://github.com/AntorDOS)

---

## ⭐ Support

If you like this project:

* ⭐ Star the repository
* 🍴 Fork it
* 🧠 Share feedback or ideas

---

## 🧩 Future Improvements (Ideas)

* Password crack time estimation
* Custom character set selection
* Save output to file
* Wordlist-based entropy analysis

---
