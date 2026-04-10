# Level 01

## 💡 Approach
```
	I only see a document named "-" I read it, and it contains the key.
```

## 🛠️ Commands Used
```bash
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat ./-
263JGJPfgU6LtdEvgfWU1XP5yac29mFx
```

## 📝 Notes
```
When a filename starts with -, always prefix it with ./ to tell the shell it's a path — otherwise Unix interprets - as stdin, not a file.
```

## ✅ Password Found
```
263JGJPfgU6LtdEvgfWU1XP5yac29mFx
```
