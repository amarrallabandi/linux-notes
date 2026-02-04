# Linux Basics & Bash Notes

## Linux I/O Redirection (Very Important)

Linux commands communicate using streams:

* **stdin**: input
* **stdout**: normal output
* **stderr**: error output

Redirection symbols control where input comes from and where output goes.

### Output Redirection

#### `>` Overwrite (Replace)

* Sends command output to a file
* Replaces existing file content

Example:

```bash
echo "Hello" > file.txt
```

#### `>>` Append

* Sends command output to the end of a file
* Keeps existing content

Example:

```bash
echo "Another line" >> file.txt
```

### Input Redirection

#### `<<` Here Document (Multi-line Input)

* Sends multiple lines of inline text as input to a command
* Stops reading when the ending marker is reached
* Commonly used for JSON, YAML, SQL, config files

Example:

```bash
cat <<EOF > employee.json
{
  "id": 101,
  "name": "Amar",
  "role": "Data Engineer"
}
EOF
```

### One-line Intuition

* `>` → **replace**
* `>>` → **append**
* `<<` → **inline multi-line input**

---

## Basic Linux Commands

### Navigation

* `pwd` → show current directory
* `ls` → list files
* `ls -l` → detailed list
* `ls -a` → include hidden files
* `cd folder` → change directory
* `cd ..` → go up one level
* `cd ~` → go to home directory

### File & Directory Operations

* `touch file.txt` → create empty file
* `mkdir folder` → create directory
* `cp src dest` → copy file
* `cp -r dir1 dir2` → copy directory
* `mv old new` → move or rename
* `rm file` → delete file
* `rm -r folder` → delete folder (recursive)

### Viewing Files

* `cat file.txt` → view file contents
* `less file.txt` → scrollable view
* `head file.txt` → first 10 lines
* `tail file.txt` → last 10 lines

### Searching

* `grep "text" file.txt` → search text in file
* `find . -name "*.txt"` → find files

---

## Common Commands Reminder

* `cat file.txt` → read file contents
* `echo text` → print text
* `ls` → list files
* `pwd` → show current directory

---

## Notes

* `echo filename` prints the filename, not its contents
* Use `cat` or `less` to read files
* Be careful with `>` — it overwrites files

---

