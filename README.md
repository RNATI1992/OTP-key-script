# 🔐 OTP-key-script

> **CLI to manage TOTP secrets and display 6-digit codes.**  
> Secrets are stored in a password-encrypted file (OpenSSL AES-256). Add keys by pasting from Git/… or generate new ones.

---

## ✨ Features

| Feature | Description |
|--------|-------------|
| 🔑 **Add keys** | Paste existing TOTP secrets (e.g. from Git or other providers) or generate new ones |
| 📋 **List** | View all stored OTP entries |
| ⏱️ **Live codes** | Shows current 6-digit code, time left in the 30s window, and the next code |
| 🔒 **Encryption** | Secrets stored in a file encrypted with OpenSSL AES-256 |
| ⏳ **Password cache** | Password is cached for 15 minutes after first unlock |

---

## 🚀 Usage

### Commands

- **`--add`** — Add a new TOTP key (paste secret or generate)
- **`--list`** — List all stored OTP keys
- **`--generate`** — Generate a new TOTP secret
- **`--reset`** — Reset/clear stored keys (use with care)

### Typical workflow

1. Run the script and unlock with your password when prompted.
2. Use `--add` to paste a secret from Git/Google Authenticator/etc. or `--generate` for a new one.
3. Use `--list` to see all keys and their current/next codes.
4. Your password stays cached for 15 minutes so you don’t have to re-enter it for every command.

---

## 📁 What you need

- A Unix-like environment (e.g. Linux, macOS) with **OpenSSL** available for encryption/decryption.
- The script from this repo (see **Installation** or the provided archive).

---

## 📦 Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/RNATI1992/OTP-key-script.git
   cd OTP-key-script
   ```
2. Extract or place the main script in your `PATH`, or run it from the project directory.
3. Run the script; on first use you’ll set a password for the encrypted store.

---

## ⚠️ Security notes

- **Backup:** Keep a backup of your encrypted OTP file and remember your password; losing both means losing access to codes.
- **Permissions:** Restrict read/write access to the script and the encrypted file (e.g. `chmod 700` where appropriate).
- **Environment:** Avoid running on untrusted or shared machines if you care about keyloggers or memory inspection.

---

## 📄 License

See the repository for license details.

---

<p align="center">
  <sub>Built for secure, local TOTP management</sub>
</p>
