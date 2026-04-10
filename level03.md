# Level 03


## 💡 Approach
```
When I entered the "inhere" directory and run the ls command, I didn’t see anything. 
This seemed strange, so I used the -a flag to check for hidden files. 
After doing that, I found a file named "...Hiding-From-You," and when I read it, I discovered the challenge flag.
```

## 🛠️ Commands Used
```bash
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere/
bandit3@bandit:~/inhere$ ls
bandit3@bandit:~/inhere$ ls -a
.  ..  ...Hiding-From-You
bandit3@bandit:~/inhere$ cat ...Hiding-From-You
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
```

## 📝 Notes
```
To see hiden files i need to use the flag -a on ls command
```

## ✅ Password Found
```
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
```
