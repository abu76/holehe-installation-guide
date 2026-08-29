# Holehe Installation Guide

A simple guide to installing and running **Holehe** on Kali Linux using a Python virtual environment.

> ⚠️ **Ethical Use Notice:** Holehe is an OSINT tool that can check whether an email address is associated with accounts on online services. Use it only with email addresses you own or where you have explicit authorization to perform the investigation.

## 📌 What is Holehe?

**Holehe** is an open-source OSINT tool that checks whether an email address is used to register accounts on supported online services.

It can be useful for:

* OSINT research
* Security awareness
* Authorized security testing
* Digital investigations
* Learning email-based reconnaissance

## 🖥️ Requirements

* Kali Linux
* Python 3
* pip
* Python virtual environment
* Internet connection

## 🚀 Installation

### 1. Update Kali Linux

```bash
sudo apt update
```

### 2. Install Python requirements

```bash
sudo apt install python3 python3-pip python3-venv -y
```

### 3. Create a virtual environment

```bash
python3 -m venv ~/holehe-env
```

### 4. Activate the virtual environment

```bash
source ~/holehe-env/bin/activate
```

Your terminal should now show something similar to:

```text
(holehe-env) user@kali:~$
```

### 5. Install Holehe

```bash
pip install holehe
```

### 6. Verify the installation

```bash
holehe --help
```

If the installation was successful, Holehe's help information should be displayed.

## 🔎 Basic Usage

With the virtual environment activated:

```bash
holehe your-email@example.com
```

Replace `your-email@example.com` with an email address you are authorized to investigate.

### Example

```bash
holehe test@example.com
```
<img width="987" height="647" alt="Holehe " src="https://github.com/user-attachments/assets/3b7614d6-b7ad-4e2e-8702-6993aa47f32d" />

## ❌ Troubleshooting

### `holehe: command not found`

First make sure the virtual environment is activated:

```bash
source ~/holehe-env/bin/activate
```

Then verify:

```bash
which holehe
```

You can also try:

```bash
python3 -m holehe --help
```

If Holehe is not installed:

```bash
pip install holehe
```

### Check the installed package

```bash
pip show holehe
```

### Upgrade Holehe

```bash
pip install --upgrade holehe
```

## 🧹 Deactivate the Virtual Environment

When finished:

```bash
deactivate
```

To use Holehe again later:

```bash
source ~/holehe-env/bin/activate
```

## 📚 Quick Installation

For users who want the complete installation sequence:

```bash
sudo apt update
sudo apt install python3 python3-pip python3-venv -y
python3 -m venv ~/holehe-env
source ~/holehe-env/bin/activate
pip install holehe
holehe --help
```

## 🔐 Responsible Use

Use Holehe responsibly.

Do not use this tool to:

* Investigate people without authorization
* Harass or target individuals
* Collect personal information for malicious purposes
* Circumvent privacy or security controls

Use it for your own accounts, authorized security testing, education, and legitimate OSINT research.

## ⭐ Contributing

Contributions are welcome.

If you find an installation issue or have an improvement for this guide, open an issue or submit a pull request.

## LICENSE

For the documentation repo, you can use the MIT License if you are licensing your own documentation. Don't claim that license applies to the Holehe software itself; Holehe's own licensing remains separate.
