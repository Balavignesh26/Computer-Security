**Hybrid Cryptography using AES, RSA, and Camellia**

A secure encryption framework that combines AES, RSA, and Camellia to provide multi-layered protection for text, images, audio, and video files. This hybrid approach enhances confidentiality, prevents key interception, and improves resilience against brute-force and differential attacks.

![Encryption Overview](https://i.imgur.com/nwrclvV.png)

---

🧠 Key Concepts

| Technique                  | Role                                           |
| -------------------------- | ---------------------------------------------- |
| 🔒 **AES (CBC Mode)**      | Fast symmetric encryption for half of the data |
| 🔐 **Camellia (CBC Mode)** | Symmetric encryption for the other half        |
| 🔑 **RSA**                 | Asymmetric encryption for secure key exchange  |
| 🧬 **Hybrid Model**        | AES + Camellia (symmetric) + RSA (asymmetric)  |

---

🚀 Features

* 🔐 **Triple-layer security** using hybrid encryption.
* 📂 Supports encryption of:

  * Text Files
  * Images
  * Audio
  * Videos (with frame length preservation)
* 📊 Performance-tested with multiple file types.
* 🔄 Fully reversible encryption with accurate decryption.

---

🧪 Simple Algorithm Overview

🔑 Key Generation & Exchange

```text
1. Receiver generates RSA key pair (public + private).
2. Sender generates AES and Camellia keys.
3. Sender encrypts these keys using receiver’s RSA public key.
```

🔄 Encryption Workflow (Sender)

```text
1. Input file → split into 2 parts.
2. Part A → encrypted with AES (CBC).
3. Part B → encrypted with Camellia (CBC).
4. Combine AES + Camellia ciphertext + IVs + encrypted keys.
5. Transmit final encrypted package.
```

🔓 Decryption Workflow (Receiver)

```text
1. Decrypt AES and Camellia keys using RSA private key.
2. Decrypt both parts using respective keys and IVs.
3. Reconstruct original file (text/image/video/audio).
```

---

🧰 Tech Stack

* 💻 Python (Jupyter Notebooks)
* 📦 `cryptography` library (AES, RSA, Camellia)
* 🖼️ OpenCV for image and video handling
* 🔊 `wave` and `pydub` for audio processing

---

📸 Screenshots & Outputs

> ✅ Key Generation
> ![Key Generation](https://i.imgur.com/9MdOGE5.png)

> 🔐 Encryption Process
> ![Encryption](https://i.imgur.com/tzW8Bv6.png)

> 🔓 Decryption Result
> ![Decryption](https://i.imgur.com/2XvT7K7.png)

---

📈 Results & Performance

| Metric                 | Result                                        |
| ---------------------- | --------------------------------------------- |
| 🔄 Decryption Accuracy | ✅ 100%                                        |
| 📹 Video Support       | ✅ Frame integrity maintained                  |
| ⚡ Encryption Speed     | ⚖️ Balanced across file types                 |
| 🔐 Security            | ✅ Resistant to brute-force & key interception |


---

🧠 Future Scope

* 🧬 Integrate post-quantum encryption.
* 🚅 Optimize speed for large multimedia files.
* 🔁 Add GUI or web-based interface using Flask or Gradio.

---

👨‍💻 Authors

* **K Balavignesh Reddy** – [GitHub](https://github.com/Balavignesh26)
* **R Kabin Dev**
* **P Gagan Devesh**
