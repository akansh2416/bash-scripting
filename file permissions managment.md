# 🔐 File Permissions Management in Linux

Linux file permissions control **who can read, write, or execute** files and directories. Understanding and managing permissions is essential for system security and proper access control.

---

## 📘 Introduction to File Permissions

Each file and directory in Linux has **three permission levels**:

| Level | Description |
|----|------------|
| **Owner (User)** | The creator of the file |
| **Group** | Users belonging to the assigned group |
| **Others** | All other users on the system |

### Permission Types

| Permission | Symbol | Value | Description |
|-----------|--------|-------|-------------|
| Read | `r` | 4 | View file contents |
| Write | `w` | 2 | Modify file contents |
| Execute | `x` | 1 | Run scripts or programs |

---

## 🔍 Viewing File Permissions

Check file permissions using:

```bash
ls -l filename
Example Output
text
Copy code
-rwxr--r-- 1 user group 1234 Mar 28 10:00 myfile.sh
Breakdown:

- → File type

rwx → Owner permissions

r-- → Group permissions

r-- → Others permissions

🔧 Changing Permissions with chmod
✳️ Symbolic Mode
Modify permissions using symbols:

+ add permissions

- remove permissions

= set exact permissions

bash
Copy code
chmod u+x filename                  # Add execute for user
chmod g-w filename                  # Remove write for group
chmod o=r filename                  # Set read-only for others
chmod u=rwx,g=rx,o= filename        # Custom permissions
🔢 Numeric (Octal) Mode
Each permission is represented by a number:

Permission	Value
Read	4
Write	2
Execute	1

bash
Copy code
chmod 755 filename  # User (rwx), Group (r-x), Others (r-x)
chmod 644 filename  # User (rw-), Group (r--), Others (r--)
chmod 700 filename  # User (rwx), No access for others
👤 Changing Ownership with chown
Modify file owner and group:

bash
Copy code
chown newuser filename               # Change owner
chown newuser:newgroup filename      # Change owner and group
chown :newgroup filename             # Change only group
Recursive Ownership Change
bash
Copy code
chown -R newuser:newgroup directory/
👥 Changing Group Ownership with chgrp
bash
Copy code
chgrp newgroup filename              # Change group
chgrp -R newgroup directory/         # Change group recursively
⭐ Special Permissions
🔑 SetUID (User ID)
Allows users to run a file with the file owner's permissions.

bash
Copy code
chmod u+s filename
📌 Example: /usr/bin/passwd

🔐 SetGID (Group ID)
Files: Run with group permissions

Directories: New files inherit the group

bash
Copy code
chmod g+s filename
chmod g+s directory/
📌 Sticky Bit
Allows only the file owner to delete files within a directory.

bash
Copy code
chmod +t directory/
📌 Example: /tmp

⚙️ Default Permissions with umask
umask defines default permissions for newly created files and directories.

View Current umask
bash
Copy code
umask
Set a New umask
bash
Copy code
umask 022   # Directories: 755 | Files: 644
✅ Conclusion
Understanding Linux file permissions is critical for system security and proper file management. With chmod, chown, chgrp, and special permissions, you can precisely control access to files and directories.
