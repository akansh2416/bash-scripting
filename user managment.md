
# User Management in Linux

## Introduction to User Management in Linux
Linux is a multi-user operating system, meaning multiple users can operate on a system simultaneously. Proper user management ensures security, controlled access, and system integrity.

## Key Files Involved in User Management

- `/etc/passwd` – Stores user account details  
- `/etc/shadow` – Stores encrypted user passwords  
- `/etc/group` – Stores group information  
- `/etc/gshadow` – Stores secure group details  

---

## Creating Users in Linux

### `useradd` Command (Most Linux Distributions)

Create a user without a home directory:
```bash
useradd username
````

Create a user with a home directory:

```bash
useradd -m username
```

Specify a default shell:

```bash
useradd -s /bin/bash username
```

### `adduser` Command (Debian-Based Systems)

```bash
adduser username
```

This interactive command prompts for a password and additional user details.

---

## Managing User Passwords

Set or change a user’s password:

```bash
passwd username
```

### Enforcing Password Policies

Set password expiration (e.g., 90 days):

```bash
chage -M 90 username
```

Lock a user account:

```bash
passwd -l username
```

Unlock a user account:

```bash
passwd -u username
```

---

## Modifying Users

Modify existing users using `usermod`.

Change the username:

```bash
usermod -l new_username old_username
```

Change the home directory:

```bash
usermod -d /new/home/directory -m username
```

Change the default shell:

```bash
usermod -s /bin/zsh username
```

---

## Deleting Users

Remove a user but keep their home directory:

```bash
userdel username
```

Remove a user and their home directory:

```bash
userdel -r username
```

---

## Working with Groups

### Creating Groups

```bash
groupadd groupname
```

### Adding Users to Groups

```bash
usermod -aG groupname username
```

### Viewing Group Memberships

```bash
groups username
```

### Changing the Primary Group

```bash
usermod -g new_primary_group username
```

---

## Sudo Access and Privilege Escalation

### Adding a User to the Sudo Group

**Debian-based systems:**

```bash
usermod -aG sudo username
```

**RHEL-based systems:**

```bash
usermod -aG wheel username
```

### Granting Specific Commands with Sudo

Edit the sudoers file safely:

```bash
visudo
```

Add the following line:

```bash
username ALL=(ALL) NOPASSWD: /path/to/command
```

---

## Summary

User management in Linux involves creating and maintaining users, managing passwords, assigning groups, and controlling administrative privileges. Proper configuration enhances system security and ensures efficient access control.

```
```

