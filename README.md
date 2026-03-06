# OTP-key-script
CLI to manage TOTP secrets and show 6-digit codes. Secrets are stored in a password-encrypted file (OpenSSL AES-256). Add keys by pasting from Git/... or generate news (--add, --list,   --generate, --reset). Shows current code, time left in the 30s window, and the next code. Password is cached for 15 minutes after first unlock. Includes README.
