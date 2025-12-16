# ⚙️ Process Management in Linux

Process management in Linux allows you to **monitor, control, and optimize running programs**. Each process has a unique **Process ID (PID)** and typically belongs to a parent process.

---

## 📘 Introduction to Process Management

A **process** is an instance of a running program. Linux provides powerful utilities to:
- View running processes
- Control execution (stop, resume, kill)
- Manage process priority
- Handle background jobs and system daemons

---

## 🔍 Viewing Processes

### Using ps
```bash
ps aux                    # View all running processes
ps -u username            # View processes for a specific user
ps -C processname         # Show a process by name
Using pgrep
bash
Copy code
pgrep processname         # Find PID(s) of a process by name
Using pidof
bash
Copy code
pidof processname         # Find PID of a running program
🛑 Managing Processes
Killing Processes
bash
Copy code
kill PID                  # Terminate a process by PID
pkill processname         # Terminate a process by name
kill -9 PID               # Force kill a process
pkill -9 processname      # Kill all instances of a process
Stopping & Resuming Processes
bash
Copy code
kill -STOP PID            # Stop a running process
kill -CONT PID            # Resume a stopped process
Changing Process Priority
bash
Copy code
top                       # View priorities (NI column)
renice -n 10 -p PID       # Lower priority (positive value)
renice -n -5 -p PID       # Increase priority (root required)
🧵 Background & Foreground Processes
Running Jobs in Background
bash
Copy code
command &                 # Run a command in the background
jobs                      # List background jobs
Foreground & Job Control
bash
Copy code
fg %jobnumber             # Bring job to foreground
Ctrl + Z                  # Suspend a running process
bg %jobnumber             # Resume a suspended job in background
📊 Monitoring System Processes
Using top
bash
Copy code
top                       # Interactive process viewer
Common Controls:

k → Kill a process (enter PID)

r → Change process priority

q → Quit

Using htop
bash
Copy code
htop                      # User-friendly process viewer (if installed)
✔ Mouse-based interaction
✔ Color-coded output

⚙️ Process Priority Management
Using nice
bash
Copy code
nice -n 10 command        # Run a command with lower priority
Using renice
bash
Copy code
renice -n -5 -p PID       # Change priority of an existing process
🧩 Daemon Process Management
Viewing Services
bash
Copy code
systemctl list-units --type=service
Managing Services
bash
Copy code
systemctl start service-name
systemctl stop service-name
systemctl enable service-name
✅ Conclusion
Effective process management is essential for system performance, stability, and control. By mastering tools like ps, top, htop, kill, nice, and systemctl, you gain full visibility and authority over Linux processes and services.
