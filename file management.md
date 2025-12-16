````md
# File Management in Linux

## File and Directory Management

- `ls` – Lists files and directories in the current location  
- `cd /path/to/directory` – Changes the working directory  
- `pwd` – Prints the current working directory  
- `mkdir new_folder` – Creates a new directory  
- `rmdir empty_folder` – Removes an empty directory  
- `rm file.txt` – Deletes a file  
- `rm -r folder` – Deletes a folder and its contents recursively  
- `cp file1.txt file2.txt` – Copies a file  
- `cp -r dir1 dir2` – Copies a directory recursively  
- `mv old_name new_name` – Moves or renames a file or directory  

---

## File Viewing and Editing

- `cat file.txt` – Displays file content  
- `tac file.txt` – Displays file content in reverse order  
- `less file.txt` – Opens a file for viewing with scrolling support  
- `more file.txt` – Similar to `less`, but only allows forward navigation  
- `head -n 10 file.txt` – Displays the first 10 lines of a file  
- `tail -n 10 file.txt` – Displays the last 10 lines of a file  
- `nano file.txt` – Opens a simple text editor  
- `vi file.txt` – Opens a powerful text editor  

---

## Writing to Files

Overwrite existing content:
```bash
echo "Hello" > file.txt
````

Append content without overwriting:

```bash
echo "Hello" >> file.txt
```

---

## Summary

File management in Linux includes creating, deleting, copying, moving, viewing, and editing files and directories. Mastery of these commands is essential for effective system navigation and administration.

```
```
