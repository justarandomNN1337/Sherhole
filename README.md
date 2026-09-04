# 🕵️ SherHole

**SherHole** is a lightweight command-line wrapper that combines [Sherlock](https://github.com/sherlock-project/sherlock) username reconnaissance with [Holehe](https://github.com/megadose/holehe) email reconnaissance.

It provides a simple interactive interface for running either tool individually or running both during the same investigation, while automatically organizing results into timestamped directories.

> **For authorized security research, OSINT, CTFs, and educational use.**

---

## ✨ Features

* 🔎 **Sherlock username reconnaissance**
* 📧 **Holehe email reconnaissance**
* 🔄 Run Sherlock, Holehe, or both
* 📁 Automatically creates the results directory
* 🕐 Timestamped directories for each investigation
* 💾 Automatically saves results
* 🖥️ Interactive terminal interface
* 🌍 Run `sherhole` from anywhere
* 🐍 Written in Python
* 🐧 Designed for Linux / Parrot OS

---

## 📂 Results

SherHole automatically stores results in:

```text
~/Desktop/recon/sherhole/
```

Each execution receives its own timestamped directory:

```text
Desktop/
└── recon/
    └── sherhole/
        ├── 2026-09-04_01-30-22/
        │   ├── sherlock_username.txt
        │   └── holehe_email_at_example.com.txt
        │
        └── 2026-09-04_02-15-47/
            └── sherlock_anotheruser.txt
```

Previous investigations are not overwritten.

---

## 🛠️ Requirements

SherHole requires:

* Python 3
* Sherlock
* Holehe
* pipx (recommended)
* Linux

### Sherlock

The recommended installation method for Sherlock is:

```bash
pipx install sherlock-project
```

Verify:

```bash
sherlock --version
```

Sherlock's official documentation recommends `pipx` and notes that the ParrotOS package can lag behind or have issues.

### Holehe

Install Holehe with:

```bash
pipx install holehe
```

Verify:

```bash
holehe --help
```

---

## 📥 Installation

Clone the repository:

```bash
git clone https://github.com/justarandomNN1337/Sherhole.git
```

Enter the directory:

```bash
cd Sherhole
```

Make the script executable:

```bash
chmod +x sherhole
```

Install it into your local executable path:

```bash
mkdir -p ~/.local/bin
cp sherhole ~/.local/bin/sherhole
```

Make sure `~/.local/bin` is in your PATH:

```bash
pipx ensurepath
```

Restart your terminal.

You should now be able to run SherHole from anywhere:

```bash
sherhole
```

---

## 🚀 Usage

Start SherHole:

```bash
sherhole
```

You'll see:

```text
============================================================
                    SHERHOLE
             Sherlock + Holehe
============================================================

1) Sherlock username
2) Holehe email
3) Both
4) Exit

Choice:
```

### 1 — Username reconnaissance

Select:

```text
1
```

Then enter a username:

```text
Username: exampleuser
```

Sherlock will run and save its results automatically.

### 2 — Email reconnaissance

Select:

```text
2
```

Then enter an email:

```text
Email: example@example.com
```

Holehe will run and its output will be saved automatically.

### 3 — Run both

Select:

```text
3
```

SherHole will:

1. Ask for a username
2. Run Sherlock
3. Wait for Sherlock to finish
4. Ask for an email
5. Run Holehe
6. Save both sets of results in the same investigation directory

---

## 🔧 Running Sherlock Manually

SherHole is a wrapper around Sherlock rather than a replacement for it.

You can still use Sherlock directly:

```bash
sherlock username
```

Sherlock also supports saving output to a specified file.

---

## 🔧 Running Holehe Manually

Holehe can also be run independently:

```bash
holehe email@example.com
```

---

## 🧠 Why SherHole?

Running multiple OSINT tools manually can quickly become messy, especially when conducting several investigations.

SherHole provides a small layer of organization by putting related results together:

```text
Investigation
     │
     ├── Sherlock
     │     └── username results
     │
     └── Holehe
           └── email results
```

This makes it easier to keep different investigations separated and review results later.

---

## ⚠️ Responsible Use

SherHole is intended for:

* Authorized security research
* OSINT research
* Capture-the-Flag (CTF) environments
* Penetration testing with permission
* Security education
* Research involving accounts or identities you are authorized to investigate

Do **not** use SherHole to harass, stalk, impersonate, dox, or otherwise target people without authorization.

The developer of SherHole is not responsible for misuse of this software.

SherHole relies on third-party projects including Sherlock and Holehe. Users should review and comply with the terms, policies, and applicable laws associated with those projects and the services they query.

---

## 📜 License

This project is provided for educational and authorized security-research purposes.

SherHole itself is a wrapper around third-party tools and does not claim ownership of Sherlock or Holehe.

See the respective projects for their licensing information:

* Sherlock: https://github.com/sherlock-project/sherlock
* Holehe: https://github.com/megadose/holehe

---

## 👤 Author

Created by **justarandomNN1337**

GitHub:

https://github.com/justarandomNN1337

Project:

https://github.com/justarandomNN1337/Sherhole

---

## ⭐ Support

If you find SherHole useful, consider giving the repository a ⭐ on GitHub.

Pull requests, bug reports, and improvements are welcome.
