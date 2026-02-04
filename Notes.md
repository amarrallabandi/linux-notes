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

(You can keep extending this document as you learn more Linux and Bash concepts.)

