# 📁 File Management in Linux

Modern Linux file management focuses on speed, clarity, and safety when working with files and directories from the command line.

---

## 📂 File & Directory Operations

| Command | Description |
|------|------------|
| `ls` | List files and directories |
| `cd /path/to/dir` | Change directory |
| `pwd` | Show current directory |
| `mkdir new_folder` | Create a directory |
| `rmdir empty_folder` | Remove an empty directory |
| `rm file.txt` | Delete a file |
| `rm -r folder` | Delete a directory recursively |
| `cp file1.txt file2.txt` | Copy a file |
| `cp -r dir1 dir2` | Copy a directory recursively |
| `mv old_name new_name` | Move or rename files/directories |

---

## 👀 Viewing Files

| Command | Description |
|------|------------|
| `cat file.txt` | Display file contents |
| `tac file.txt` | Display contents in reverse |
| `less file.txt` | Scrollable file viewer |
| `more file.txt` | Forward-only viewer |
| `head -n 10 file.txt` | Show first 10 lines |
| `tail -n 10 file.txt` | Show last 10 lines |

---

## ✏️ Editing Files

| Command | Description |
|------|------------|
| `nano file.txt` | Simple terminal text editor |
| `vi file.txt` | Advanced terminal editor |

---

## 📝 Writing to Files

Overwrite file content:
```bash
echo "Hello" > file.txt
Append content:

bash
Copy code
echo "Hello" >> file.txt
⚡ Pro Tips
Use ls -lh for human-readable file sizes

Combine commands with pipes (|) for powerful workflows

Use rm -i to avoid accidental deletions

Prefer less over cat for large files

✅ Summary
Linux file management is built around powerful, composable commands. Understanding these tools enables efficient navigation, editing, and automation in modern Linux environments.
