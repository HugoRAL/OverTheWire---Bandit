# Level 05


## 💡 Approach
```
When I entered the "inhere" directory and ran the ls command, I saw multiple directories with several files inside. 
I reread the challenge and noticed the clue: "1033 bytes in size." Based on that, I used the find command to search for a file with that exact size. 
The search returned the file "./maybehere07/.file2." When I read it, I discovered the challenge flag.
```

## 🛠️ Commands Used
```bash
bandit5@bandit:~$ ls -a
.  ..  .bash_logout  .bashrc  inhere  .profile
bandit5@bandit:~$ cd inhere/
bandit5@bandit:~/inhere$ ls -a
.            maybehere01  maybehere04  maybehere07  maybehere10  maybehere13  maybehere16  maybehere19
..           maybehere02  maybehere05  maybehere08  maybehere11  maybehere14  maybehere17
maybehere00  maybehere03  maybehere06  maybehere09  maybehere12  maybehere15  maybehere18
bandit5@bandit:~/inhere$ find ./* -size 1033c
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
```

## 📝 Notes
```
On flag -size i must never forget the units in the end
```

## ✅ Password Found
```
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
```
