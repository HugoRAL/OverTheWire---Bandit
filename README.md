<div align="center">

# 🏴‍☠️ OverTheWire: Bandit

### My personal walkthrough, notes & command reference for the Bandit wargame

[![OverTheWire](https://img.shields.io/badge/OverTheWire-Bandit-red?style=for-the-badge&logo=linux&logoColor=white)](https://overthewire.org/wargames/bandit/)
[![Progress](https://img.shields.io/badge/Progress-In%20Progress-yellow?style=for-the-badge)](#-progress)
[![Levels](https://img.shields.io/badge/Levels-0%20→%2033-blue?style=for-the-badge)](#-levels)

</div>

---

## 🧭 What is Bandit?

[Bandit](https://overthewire.org/wargames/bandit/) is a beginner-friendly **wargame** hosted by [OverTheWire](https://overthewire.org). It's designed to teach the fundamentals of the Linux command line, shell scripting, file permissions, networking, encoding, and much more — all through a series of progressive challenges.

Each level requires you to find a password hidden somewhere on a remote Linux machine. That password is used to SSH into the next level. The difficulty increases steadily, building skills layer by layer.

> *"The Bandit wargame is aimed at absolute beginners. It will teach the basics needed to be able to play other wargames."*
> — OverTheWire

---

## 🎯 Why I'm Doing This

I started Bandit to sharpen my command-line intuition, get comfortable with Linux internals, and build a stronger foundation in cybersecurity concepts. As a developer working with legacy systems and backend infrastructure, these low-level skills are invaluable.

This repository serves as my **personal knowledge base** — a place to document my thought process, the commands I discover, and the lessons I take away from each level.

---

## 📁 Repository Structure

```
otw-bandit/
├── README.md                    ← You are here
├── commands-reference.md        ← Every command I've learned, categorised
└── levels/
    ├── level00-01.md            ← Notes for Level 0 → 1
    ├── level01-02.md            ← Notes for Level 1 → 2
    ├── level02-03.md
    │   ...
    └── level33-34.md            ← Notes for Level 33 → 34
```

Each level file follows a consistent format:

- **🎯 Goal** — what the challenge asks you to do
- **🔗 Resources** — relevant man pages or hints
- **💡 Approach** — my reasoning and thought process
- **🛠️ Commands Used** — exact commands that led to the solution
- **📝 Notes** — observations, gotchas, and things I want to remember
- **✅ Password Found** — *(optional, kept private)*

---

## 📖 Commands Reference

All commands and concepts I've picked up are catalogued in [`commands-reference.md`](./commands-reference.md), organized by category:

| Category | Topics Covered |
|----------|---------------|
| 📁 File System | `ls`, `find`, `file`, navigation |
| 🔍 Reading & Searching | `grep`, `sort`, `uniq`, `strings`, `xxd` |
| 🔐 Permissions | `chmod`, `chown`, `sudo`, `id` |
| ⚙️ Processes & Env | `ps`, `env`, `export`, `cron` |
| 🌐 Networking | `ssh`, `nc`, `nmap`, `openssl` |
| 🔒 Encoding | `base64`, `tr`, `gpg`, `openssl enc` |
| 📦 Compression | `tar`, `gzip`, `bzip2`, `zip` |
| 🌿 Git | `log`, `show`, `stash`, `branch`, `tag` |
| 🎩 Tricks | pipes, redirects, wildcards, special filenames |

---

## 📊 Progress

| Level | Status | Key Concept |
|-------|--------|-------------|
| 0 → 1 | ✅ | SSH basics |
| 1 → 2 | ✅ | Files with special names |
| 2 → 3 | ✅ | Spaces in filenames |
| 3 → 4 | ✅ | Hidden files |
| 4 → 5 | ✅ | File types |
| 5 → 6 | ✅ | `find` with properties |
| 6 → 7 | 🟡 | Find by owner/group/size |
| 7 → 8 | ⬜ | `grep` in large files |
| 8 → 9 | ⬜ | `sort` + `uniq` |
| 9 → 10 | ⬜ | `strings` on binary |
| 10 → 11 | ⬜ | Base64 decoding |
| 11 → 12 | ⬜ | ROT13 / `tr` |
| 12 → 13 | ⬜ | Hexdump + multiple compressions |
| 13 → 14 | ⬜ | SSH with private key |
| 14 → 15 | ⬜ | Netcat (`nc`) |
| 15 → 16 | ⬜ | SSL/TLS (`openssl s_client`) |
| 16 → 17 | ⬜ | Port scanning (`nmap`) |
| 17 → 18 | ⬜ | `diff` between files |
| 18 → 19 | ⬜ | SSH non-interactive commands |
| 19 → 20 | ⬜ | SetUID binaries |
| 20 → 21 | ⬜ | Netcat + background jobs |
| 21 → 22 | ⬜ | Cron jobs |
| 22 → 23 | ⬜ | Reading cron scripts |
| 23 → 24 | ⬜ | Writing cron scripts |
| 24 → 25 | ⬜ | Brute-forcing with bash |
| 25 → 26 | ⬜ | Restricted shell escape |
| 26 → 27 | ⬜ | Restricted shell + vim |
| 27 → 28 | ⬜ | Git clone |
| 28 → 29 | ⬜ | Git log / history |
| 29 → 30 | ⬜ | Git branches |
| 30 → 31 | ⬜ | Git tags |
| 31 → 32 | ⬜ | Git push |
| 32 → 33 | ⬜ | Uppercase shell escape |
| 33 → 34 | ⬜ | Final level |

> ⬜ Not started &nbsp; 🟡 In progress &nbsp; ✅ Completed

---

## 🚀 How to Connect

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
# Password: bandit0
```

Each subsequent level:

```bash
ssh bandit<N>@bandit.labs.overthewire.org -p 2220
```

---

## 📌 Key Takeaways

> *(Updated as I progress)*

- The `file` command is your best friend when dealing with unknown data
- Always try `man <command>` before Googling — the answer is often right there
- `find` is incredibly powerful with the right flags (`-size`, `-user`, `-perm`, `-type`)
- Piping commands together (`|`) is the Linux superpower
- Never underestimate what you can do with basic tools creatively combined

---

## ⚠️ Disclaimer

This repository contains **my personal notes and thought processes** — not copy-pasted solutions. The goal is learning, not spoilers.

If you're working through Bandit yourself, I'd encourage you to attempt each level independently before looking at anyone else's notes. The struggle is where the learning happens. 💪

---

## 🔗 Useful Links

- [OverTheWire: Bandit](https://overthewire.org/wargames/bandit/) — Official challenge page
- [ExplainShell](https://explainshell.com) — Understand any shell command
- [TLDRPages](https://tldr.sh) — Quick command references
- [GTFOBins](https://gtfobins.github.io) — Unix binary abuse techniques (useful later!)

---

<div align="center">

Made with 🖥️ and too much ☕ by **Hugo**

*Learning one level at a time.*

</div>
