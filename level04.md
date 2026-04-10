# Level 04


## 💡 Approach
```
When I entered the "inhere" directory and run the ls command, I saw multiple files, most of which contained unusual or unreadable text.
This seemed strange, so I used the "file" command to check their file extension. 
After doing that, I found a file named "-file07" that was identified as a normal text file. 
When I read it, I discovered the challenge flag.
```

## 🛠️ Commands Used
```bash
bandit4@bandit:~$ ls -a
.  ..  .bash_logout  .bashrc  inhere  .profile
bandit4@bandit:~$ cd inhere/
bandit4@bandit:~/inhere$ ls -a
.  ..  -file00  -file01  -file02  -file03  -file04  -file05  -file06  -file07  -file08  -file09
bandit4@bandit:~/inhere$ file ./-file0*
./-file00: data
./-file01: data
./-file02: data
./-file03: DOS executable (COM), start instruction 0x8c887e10 c3ee96c9
./-file04: data
./-file05: data
./-file06: data
./-file07: ASCII text
./-file08: data
./-file09: data
bandit4@bandit:~/inhere$ cat ./-file07
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
bandit4@bandit:~/inhere$
```

## 📝 Notes
```
-To see multiple files use *
-Pay attention on file extension (use the file command)
```

## ✅ Password Found
```
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
```
