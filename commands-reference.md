# 📚 Commands Reference — OverTheWire Bandit

A living document of every command and concept I encountered while solving Bandit.
Updated as I progress through the levels.

---

## 🗂️ Table of Contents

- [File System Navigation](#-file-system-navigation)
- [File Reading & Searching](#-file-reading--searching)
- [Permissions & Ownership](#-permissions--ownership)
- [Processes & Environment](#-processes--environment)
- [Networking](#-networking)
- [Encoding & Encryption](#-encoding--encryption)
- [Compression & Archives](#-compression--archives)
- [Git](#-git)
- [Miscellaneous / Tricks](#-miscellaneous--tricks)

---

## 📁 File System Navigation

| Command | Description | Example |
|---------|-------------|---------|
| `ls` | List directory contents | `ls -la` |
| `cd` | Change directory | `cd /tmp` |
| `pwd` | Print working directory | `pwd` |
| `find` | Search for files | `find / -name "*.txt" 2>/dev/null` |
| `file` | Determine file type | `file mystery_file` |
| `du` | Disk usage | `du -sh *` |

---

## 🔍 File Reading & Searching

| Command | Description | Example |
|---------|-------------|---------|
| `cat` | Print file contents | `cat readme.txt` |
| `less` | Page through a file | `less bigfile.txt` |
| `more` | Page through a file | `more bigfile.txt` |
| `head` | First N lines | `head -n 20 file.txt` |
| `tail` | Last N lines | `tail -n 20 file.txt` |
| `strings` | Print printable strings in binary | `strings data.bin` |
| `grep` | Search text patterns | `grep -r "password" .` |
| `sort` | Sort lines | `sort file.txt` |
| `uniq` | Filter duplicate lines | `sort file.txt \| uniq -u` |
| `wc` | Word/line count | `wc -l file.txt` |
| `diff` | Compare files | `diff file1 file2` |
| `xxd` | Hex dump | `xxd file.bin` |

---

## 🔐 Permissions & Ownership

| Command | Description | Example |
|---------|-------------|---------|
| `chmod` | Change file permissions | `chmod 700 script.sh` |
| `chown` | Change file owner | `chown user:group file` |
| `ls -la` | List with permissions | `ls -la /etc/passwd` |
| `id` | Show current user/group IDs | `id` |
| `whoami` | Current username | `whoami` |
| `su` | Switch user | `su bandit7` |
| `sudo` | Execute as superuser | `sudo -l` |

---

## ⚙️ Processes & Environment

| Command | Description | Example |
|---------|-------------|---------|
| `ps` | List processes | `ps aux` |
| `top` | Live process monitor | `top` |
| `env` | Print environment variables | `env` |
| `export` | Set environment variable | `export VAR=value` |
| `echo` | Print to stdout | `echo $PATH` |
| `which` | Locate a command | `which python3` |
| `nc` | Netcat — networking Swiss Army knife | `nc localhost 30000` |
| `cron` / `crontab` | Scheduled tasks | `crontab -l` |

---

## 🌐 Networking

| Command | Description | Example |
|---------|-------------|---------|
| `ssh` | Secure shell | `ssh bandit0@bandit.labs.overthewire.org -p 2220` |
| `nc` (netcat) | Open TCP/UDP connections | `nc -l 1234` |
| `nmap` | Network scanner | `nmap -p- localhost` |
| `curl` | Transfer data from URLs | `curl http://example.com` |
| `wget` | Download files | `wget http://example.com/file` |
| `openssl s_client` | SSL/TLS connection | `openssl s_client -connect host:port` |

---

## 🔒 Encoding & Encryption

| Command | Description | Example |
|---------|-------------|---------|
| `base64` | Encode/decode base64 | `echo "text" \| base64` / `base64 -d` |
| `xxd` | Hex encode/decode | `xxd -r -p hex.txt` |
| `tr` | Translate/rotate characters (ROT13) | `echo "text" \| tr 'A-Za-z' 'N-ZA-Mn-za-m'` |
| `openssl enc` | Symmetric encryption | `openssl enc -aes-256-cbc -d -in file` |
| `gpg` | GNU Privacy Guard | `gpg --decrypt file.gpg` |
| `md5sum` | Compute MD5 hash | `md5sum file` |
| `sha256sum` | Compute SHA-256 hash | `sha256sum file` |

---

## 📦 Compression & Archives

| Command | Description | Example |
|---------|-------------|---------|
| `tar` | Archive utility | `tar -xvf file.tar` |
| `gzip` / `gunzip` | Compress/decompress .gz | `gunzip file.gz` |
| `bzip2` / `bunzip2` | Compress/decompress .bz2 | `bunzip2 file.bz2` |
| `zip` / `unzip` | Zip archives | `unzip file.zip` |
| `file` | Always run this first on unknown blobs! | `file data` |

---

## 🌿 Git

| Command | Description | Example |
|---------|-------------|---------|
| `git log` | View commit history | `git log --oneline` |
| `git show` | Show a commit's content | `git show <hash>` |
| `git branch -a` | List all branches | `git branch -a` |
| `git checkout` | Switch branch/commit | `git checkout <branch>` |
| `git stash list` | List stashed changes | `git stash list` |
| `git stash show` | Show stash contents | `git stash show -p` |
| `git tag` | List tags | `git tag` |
| `git diff` | Show changes | `git diff HEAD~1` |

---

## 🎩 Miscellaneous / Tricks

| Trick | Description | Example |
|-------|-------------|---------|
| Redirect stderr | Hide error messages | `command 2>/dev/null` |
| Pipe `\|` | Chain commands | `cat file \| grep pattern` |
| Command substitution | Use output as argument | `$(command)` |
| Wildcard `*` | Match any characters | `ls *.txt` |
| Tilde `~` | Home directory shortcut | `cd ~` |
| `-` as stdin | Read from pipe | `cat - > file` |
| `/dev/null` | Discard output | `command > /dev/null` |
| Escape spaces in filenames | Quote or backslash | `cat "file name"` or `cat file\ name` |
| Read files with special names | Use `./` prefix | `cat ./-filename` |

---

> 💡 **Tip:** When stuck, always try `man <command>` or `<command> --help` first.
> The Bandit challenges are intentionally designed to teach you to read documentation!
