# Level 06


## 💡 Approach
```
When I started this challenge, I didn’t find any relevant directories, so I decided to use the find command from the root of the filesystem.
Based on the challenge instructions, I searched for a file with the following properties:
owned by user bandit7
owned by group bandit6
33 bytes in size
I used this command:
find / -size 33c -group bandit6 -user bandit7 -readable
However, the command returned a lot of unwanted output due to permission errors, such as:
find: '/var/cache/apt/archives/partial': Permission denied
To suppress these error messages, I redirected the error output using:
2>/dev/null
Final command:
find / -size 33c -group bandit6 -user bandit7 -readable 2>/dev/null
This works because:
2 represents stderr (error output)
> redirects the output
/dev/null discards any data written to it
As a result, only valid matches are displayed, and the permission errors are hidden.
```

## 🛠️ Commands Used
```bash
bandit6@bandit:~$ find /* -size 33c -group bandit6 -user bandit7 -readable 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
```

## 📝 Notes
```
In Linux, we can use 2>/dev/null to suppress error messages from the output.

There are three standard communication channels:
0 — stdin (input)
1 — stdout (standard output)
2 — stderr (error output)

The expression 2>/dev/null means:
2 — the error stream (stderr)
> — redirect
/dev/null — a special file that discards any data written to it (like a black hole)
```

## ✅ Password Found
```
morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
```
