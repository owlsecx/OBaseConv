# 🦉 OBaseConv

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-Security-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0-cyan?style=flat-square"/>
</p>

> **OBaseConv** — part of the OwlSec Toolkit.

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OBaseConv handles number bases and data encodings in one tool. It converts numbers between any base from 2 to 62, encodes and decodes 24 formats from hex and Base64 to Ascii85 and uuencode, and auto-detects unknown encodings. It can peel off nested encodings layer by layer and run CyberChef-style recipe chains.

---

## ✨ Features

- Number conversion across bases 2–62 with 0x/0b/0o prefixes, negatives, two's complement (8–128 bit) and popcount
- 24 encodings: hex variants, C array, Base32/45/58/62/64/64url, Ascii85, Z85, URL, HTML, Unicode escapes, quoted-printable, uuencode
- Auto-detect ranks every decoder by confidence, and unwrap peels nested encodings
- Recipe chains such as b64d,gunzip,hexe,xor:key,rot13
- Integer ↔ bytes (endianness and widths), IEEE-754 floats, Unicode inspector and big-integer bitwise calculator
- File encode/decode and a scripting CLI (--json, --raw, stdin)

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OBaseConv                                  # interactive menu
./OBaseConv --num 0xdeadbeef
./OBaseConv --detect "SGVsbG8gT3ds"
./OBaseConv --unwrap < blob.txt
./OBaseConv --chain 'b64d,gunzip' --file payload.txt
```

Run `./OBaseConv --help` for the full list of options.

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
