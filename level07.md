# Level 07


## 💡 Approach
```
The challenge is simple find a password stored in data.txt next to the word "millionth".
The file contains a massive list of word-password pairs, so manually searching is impractical, but the ctf "next to the word millionth".
So i used the comand "grep -w millionth data.txt" to find the soluction
```

## 🛠️ Commands Used
```bash
bandit7@bandit:~$ ls
data.txt
bandit7@bandit:~$ grep -w millionth data.txt
millionth       dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
```

## 📝 Notes
```
none
```

## ✅ Password Found
```
dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
```
