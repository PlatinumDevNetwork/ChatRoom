<h4 align="center"> If you find this GitHub repo useful, please consider giving it a star! ⭐️ </h4> 

<p align="center">
  <img width="20%" src="https://github.com/spyboy-productions/CipherGist/blob/main/demo/CipherGist.webp" />
</p>

<h3 align="center">🛡️ ChatRoom - End-to-End Encrypted Messaging via GitHub Gists</h3>

ChatRoom is a lightweight, secure, and open-source encrypted messenger that enables private communication using GitHub Gists as the backend. It leverages **NaCl (libsodium)** for state-of-the-art encryption and ensures messages remain private and self-controlled.

<p align="center">
  <img width="30%" src="https://github.com/spyboy-productions/CipherGist/blob/main/demo/CipherGist.png" />
</p>

## ✨ Features  
✅ **End-to-End Encryption** – Uses **Ed25519 (signing)** and **X25519 (encryption)** for secure communication.  
✅ **No Central Server** – Messages are stored and exchanged via GitHub Gists.  
✅ **Self-Destructing Keys** – Private keys are never shared or stored remotely.  
✅ **Lightweight & Fast** – Runs in a terminal, with minimal dependencies.  
✅ **Cross-Platform** – Works on **Windows, Android(Termux), macOS, and Linux**.  
✅ **Fully Open-Source** – Code transparency ensures security.  

---

## 🔥 What Makes ChatRoom Unique?  
🔹 Unlike traditional messengers (WhatsApp, Signal), **ChatRoom does not use a central server**.  
🔹 No phone number, email, or identity required—**just a GitHub account**.  
🔹 Messages are **not stored permanently**—once deleted from Gist, they are gone forever.  
🔹 **No third-party tracking**—GitHub itself can't read your encrypted messages.  

| 🚀 **Conclusion:**  |
| ChatRoom is the **most private and self-hosted** option, ideal for those who want **no central servers, no phone numbers, and full control over encryption keys.** However, it's not as user-friendly as mainstream apps and doesn't offer multi-user group chat yet.  |

---

## 🛠️ Installation & Setup  

### 1️⃣ Installation
```bash
git clone https://github.com/PlatinumDevNetwork/ChatRoom.git
```
```
cd ChatRoom
```
```
pip install -r requirements.txt
```
### 2️⃣ Create a GitHub Account  
Go to [GitHub](https://github.com/) and create an account if you don’t have one.

### 3️⃣ Get a GitHub Token  
1. Visit: [GitHub Developer Settings](https://github.com/settings/tokens)  
2. Click **"Generate new token" (classic)**  
3. Select **"Gist"** with read, write, delete permission  
4. Copy and save your **GitHub Token** (you won’t see it again!)

### 4️⃣ Create a Gist  
1. Go to: [GitHub Gists](https://gist.github.com/)  
2. Click **"New Gist"**  
3. Name it **chat.txt** (keep it public or secret)  
4. Click **"Create gist"**  
5. Copy the **Gist ID** (last part of the URL)
<img width="100%" align="centre" src="https://github.com/platinumdevnetwork/chatroom/blob/main/demo/gist_id.png" />

### 5️⃣ Run ChatRoom  

```sh
python ChatRoom.py
```

If it’s your first time running, it will ask for:  
🔹 **GitHub Token**  
🔹 **Gist ID**  

These will be stored in `config.txt` for future use.  

---
⚠️ **IMPORTANT:**  
**Both you and your friend must use the same `config.txt` ** for the conversation to work!  

You can manually share `config.txt` with your friends or You can share it using the following method...

### To share config.txt

```
python send.py
```
```diff
- 🔐 Note: It encrypts config.txt, uploads it to a Gist, and automatically deletes it after your friend downloads and decrypts it.
```
### To Receive config.txt

```
python receiver.py
```
it will download, decrypt and save config.txt in original format and then delete the gist.

<img width="100%" align="centre" src="https://github.com/platinumdevnetwork/chatroom/blob/main/demo/send_demo.png" />
<img width="100%" align="centre" src="https://github.com/platinumdevnetwork/chatroom/blob/main/demo/recive_demo.png" />

## 🔑 How to Use  

```sh
python ChatRoom.py
```

<img width="100%" src="https://github.com/Platinumdevnetwork/Chatroom/blob/main/demo/demo.png" />

📤 **Sending a Message:**  
1. Type your message and hit Enter.  
2. The message gets encrypted and stored in your **Gist**.  
3. Your friend with the same **config.txt** can decrypt it.  

📥 **Receiving Messages:**  
1. The program checks your Gist every **3 seconds**.  
2. If a new encrypted message is found, it **automatically decrypts and displays** it.  

---

## 🔐 Is ChatRoom Secure?  
✔ **Uses NaCl cryptography (Ed25519 & X25519)** – trusted by security experts.  
✔ **No passwords stored** – keys are generated per session.  
✔ **No central server** – GitHub can't read your encrypted messages.  
✔ **No metadata leaks** – only encrypted text is uploaded to Gists.  
✔ **Self-hosted & auditable** – you control the encryption keys.  

---

## 📝 Future Plans  
🚀 **Mobile App** – A mobile version for Android/iOS.

🔒 **Multi-User Chat Support** – Secure group conversations.  

---

### 🎯 Start Encrypting Today!  
**Forget about centralized messengers.** Take control of your privacy with **ChatRoom**.

<h4 align="center"> If you find this GitHub repo useful, please consider giving it a star! ⭐️ </h4> 
