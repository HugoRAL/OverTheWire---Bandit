# Level 00 → Level 01

## 🎯 Goal
find the flag

## 🔗 Resources
<!-- none -->

## 💡 Approach
```
	I only see a document named "--spaces\ in\ this\ filename--" I read it, and it contains the key.
```

## 🛠️ Commands Used
```bash
bandit2@bandit:~$ ls
--spaces in this filename--
bandit2@bandit:~$ cat ./--spaces\ in\ this\ filename--
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
```

## 📝 Notes
<!-- When a filename starts with -, always prefix it with ./ to tell the shell it's a path — otherwise Unix interprets - as stdin, not a file. -->

## ✅ Password Found
```
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
```
