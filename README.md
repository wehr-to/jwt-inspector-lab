# 🛡️ JWT Inspector & Tamper Lab

## 🎯 Purpose
A hands-on JWT inspection lab to explore, test, and simulate vulnerabilities like:
- `alg: none` bypass
- Symmetric key used as public (key confusion)
- Weak algorithms or incorrect verification
- Forged token payloads (`admin: true`)

## 🔨 Tech Stack
- **Framework**: FastAPI
- **JWT Logic**: pyjwt, cryptography
- **Optional Frontend**: React or HTMX for visualization

## 🔐 Security Value
- **OWASP A07**: Broken Authentication
- Simulates both secure and insecure handling of JWTs
- Teaches common misconfigurations and bypasses
- Includes token replay tracking and validation trails

## 🔎 Features
- Upload JWT to inspect:
  - Signature validation
  - Expiration check
  - Header & payload visibility
- Tamper lab:
  - Try `alg: none`
  - Try HS256 key as RS256 public
  - Forge custom payloads (`{ "admin": true }`)
- Toggle validation algorithms (HS256, RS256, ES256, etc.)
- Logs all actions to `audit_log.json`

## 🚀 Getting Started
```bash
# Clone repo
$ git clone https://github.com/yourusername/jwt-inspector-lab.git
$ cd jwt-inspector-lab

# Run locally
$ python3 -m venv venv && source venv/bin/activate
$ pip install -r requirements.txt
$ python run.py

# Or run with Docker
$ docker-compose up --build
```

## ✅ To Do
- [ ] Add live visualizer with React or HTMX
- [ ] Add offline mode for local-only inspection
- [ ] Add signature strength scoring system
- [ ] Add unit tests for `forge_lab.py`

## 📄 License
MIT
