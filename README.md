# 🔐 Secure File Transfer with Cryptography

A Python-based secure file transfer application using **AES encryption** and **PBKDF2 key derivation**. The tool ensures confidentiality and integrity of files transferred over a network between a sender and a receiver. This project uses a GUI built with `Tkinter` for ease of use.

## 📌 Features

- ✅ **AES-256 encryption** for file confidentiality.
- ✅ **PBKDF2** for secure key derivation using password and salt.
- ✅ **Socket programming** for sending/receiving encrypted files.
- ✅ **Tkinter GUI** for file selection, encryption, sending and receiving.
- ✅ Cross-platform compatible (Tested on Windows and Linux).

---

## 📂 Project Structure

Secure-File-Transfer-Crypto/
├── sender.py # GUI to select, encrypt, and send files
├── receiver.py # GUI to receive and decrypt files
├── crypto_utils.py # Encryption, decryption and key generation functions
├── README.md
└── requirements.txt

pgsql
Copy
Edit

---

## 🔧 Technologies Used

- Python 3.x
- `Tkinter` – GUI
- `socket` – Network communication
- `cryptography` – AES encryption/decryption
- `os`, `hashlib`, `base64`, `threading` – standard modules

---

## 🧠 How It Works

### 1. **Encryption Process**:
- User selects a file and enters a password.
- A secure 256-bit AES key is derived from the password using PBKDF2.
- The file is encrypted with this key using AES-CBC mode.
- Encrypted file is sent over a TCP socket to the receiver.

### 2. **Decryption Process**:
- Receiver listens for incoming encrypted file.
- Once received, the user enters the same password used for encryption.
- The file is decrypted and saved locally.

---

## 🚀 Getting Started

### 🔽 Clone the Repository

```bash
git clone https://github.com/your-username/Secure-File-Transfer-Crypto.git
cd Secure-File-Transfer-Crypto
📦 Install Dependencies
bash
Copy
Edit
pip install -r requirements.txt
Make sure Python 3.8+ is installed

▶️ Run Sender (on Sender's PC)
bash
Copy
Edit
python sender.py
▶️ Run Receiver (on Receiver's PC)
bash
Copy
Edit
python receiver.py
🛡️ Security Considerations
AES-256 in CBC mode is used for encryption.

IV and Salt are randomly generated per session.

Password-based encryption ensures secure key management.

Only known users (via password sharing) can decrypt the file.

Not suitable for anonymous file transfers or key exchange over insecure channels.

📸 GUI Screenshots
(You can add screenshots of the sender and receiver GUI windows here using image links)

💡 Use Cases
Sharing confidential documents securely over LAN/WiFi.

Secure communication between two systems without third-party cloud services.

Educational demo of applied cryptography and network programming.

👨‍💻 Author
Naveen A D
Cybersecurity Associate | Ethical Hacker | Python Developer
GitHub | LinkedIn

📜 License
This project is licensed under the MIT License - see the LICENSE file for details.

🙌 Acknowledgements
Cryptography.io

Python Documentation

Real Python - Socket Programming

✅ To Do (Optional Improvements)
Add file integrity check using SHA-256 hash.

Add progress bar for large file transfers.

Encrypt filenames and metadata.

Add authentication with OTP or digital signature.

yaml
Copy
Edit

---

Let me know if your version has other encryption algorithms (e.g., RSA/AES hybrid), command-line interface, or if it's a web app — I’ll tailor it accordingly.
