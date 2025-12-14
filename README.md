# 🔐 SHA-256 Checksum Verifier (Web)

A simple, open-source, browser-based tool for verifying SHA-256 checksums of files.

This tool is designed for users who want to **independently verify the integrity and authenticity of downloaded files**, especially security-critical software such as cryptocurrency wallets.

👉 **Live version:**
[https://cryptabox.github.io/sha256-checker-web/](https://cryptabox.github.io/sha256-checker-web/)

---

## ✅ What this tool does

* Calculates the **SHA-256 checksum** of a selected file
* Compares it with an **expected checksum**
* Works **entirely in your browser**
* Requires **no installation**
* Uses the browser’s native **WebCrypto API**
* **No files are uploaded**
* **No network requests are made**

Your file never leaves your device.

---

## 🔍 Why checksum verification matters

When downloading security-sensitive software (wallets, cryptographic tools, binaries), checksum verification helps ensure that:

* the file was **not modified**
* the file was **not corrupted**
* the file was **not replaced by a malicious version**

This is a standard security practice used by professional software projects.

---

## 🧪 How to use

1. Open the web checker:
   [https://cryptabox.github.io/sha256-checker-web/](https://cryptabox.github.io/sha256-checker-web/)

2. Enter the **expected SHA-256 checksum** (provided by the software author)

3. Select the downloaded file

4. Click **“Verify checksum”**

5. Compare the result:

   * ✅ *Checksum matches* → the file is authentic
   * ❌ *Checksum does not match* → do **not** use the file

---

## 🛡 Security notes

* This tool runs **100% locally** in your browser
* It uses `crypto.subtle.digest()` (WebCrypto API)
* No JavaScript libraries, no CDN, no tracking
* You can inspect the source code yourself

If you do not trust this page, you can:

* download the HTML file
* disconnect from the internet
* open it locally in your browser

The result will be the same.

---

## 🧰 Manual verification (alternative methods)

You may also verify checksums using standard OS tools:

### Windows

```bat
certutil -hashfile yourfile.exe SHA256
```

### Linux

```bash
sha256sum yourfile.AppImage
```

### macOS

```bash
shasum -a 256 yourfile.dmg
```

---

## 🔗 About CryptaBox

This checksum verifier is published as part of the **CryptaBox** security philosophy.

**CryptaBox** is a privacy-focused cryptocurrency wallet that operates without servers, accounts, or centralized storage.
All cryptographic operations are performed locally on the user’s device.

🌐 Official website:
👉 [https://cryptabox.com](https://cryptabox.com)

The checksum tool allows users to independently verify CryptaBox binaries — or **any other file** — without trusting third-party services.

---
