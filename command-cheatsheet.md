# Linux Command Cheatsheet  
_A quick reference with explanations and practice tasks_  

---

## 1. Everyday Commands (Basics)

- `pwd` → Print working directory (shows where you are).  
- `ls` → List files in the current directory.  
- `ls -l` → Long listing (permissions, owners, file sizes, dates).  
- `ls -a` → Show hidden files (those starting with `.`).  
- `cd <dir>` → Change directory. Example: `cd Documents`.  
- `cd ..` → Move one directory up.  
- `mkdir <dir>` → Make a new directory. Example: `mkdir testfolder`.  
- `rmdir <dir>` → Remove an empty directory.  
- `touch <file>` → Create an empty file. Example: `touch notes.txt`.  
- `cp <source> <destination>` → Copy files. Example: `cp file.txt backup.txt`.  
- `mv <source> <destination>` → Move or rename files. Example: `mv old.txt new.txt`.  
- `cat <file>` → Print file contents to screen.  
- `less <file>` → Open file for reading (scroll with arrows, `q` to quit).  

---

## 2. Intermediate Commands

- `file <name>` → Show what type of file it is.  
- `find <dir> -name <filename>` → Search for a file. Example: `find . -name secret.txt`.  
- `grep "word" <file>` → Search for text inside a file. Example: `grep "password" notes.txt`.  
- `echo "text"` → Print text. Example: `echo Hello`.  
- `echo "text" > file.txt` → Overwrite file with text.  
- `echo "text" >> file.txt` → Append text to file.  
- `wc -l <file>` → Count lines in a file.  
- `wc -w <file>` → Count words in a file.  
- `head -n 10 <file>` → Show first 10 lines.  
- `tail -n 10 <file>` → Show last 10 lines.  
- `chmod <permissions> <file>` → Change file permissions. Example: `chmod 644 notes.txt`.  
- `chown <user>:<group> <file>` → Change file ownership.  

---

## 3. Gotchas (Tricky Situations)

- **Filenames with spaces**:  
  - `cat "file with spaces.txt"`  
  - OR `cat file\ with\ spaces.txt`  

- **Filenames starting with `-` (dash)**:  
  - `cat ./--weirdfile`  

- **Hidden files**:  
  - Files starting with `.` (e.g., `.hidden`). Use `ls -a` to see them.  

- **Permissions denied**:  
  - Try `sudo <command>` (if you have permissions).  
  - Or check with `ls -l` who owns the file.  

---

## 4. Practice Tasks

### Level 1: Basics
1. Show your current directory.  
2. Create a folder called `practice`.  
3. Inside `practice`, create two files: `a.txt` and `b.txt`.  
4. Copy `a.txt` into `b.txt`.  

### Level 2: Intermediate
1. Write the word `hello` into `a.txt`.  
2. Append `world` into `a.txt`.  
3. Count how many words are inside `a.txt`.  
4. Search for the word `world` inside `a.txt`.  

### Level 3: Gotchas
1. Create a file called `my file.txt` and write `secret` inside. Then read it back.  
2. Create a file called `--strange` and write `oddname` inside. Then read it back.  
3. Find all hidden files in your home directory.  
4. Try to open a file where permissions are denied (simulate with `chmod 000 file.txt`).  

---

✅ Tip: When stuck, remember — the shell sees **spaces and dashes** differently. Use quotes (`"..."`) or escapes (`\`) to talk to it clearly.  

