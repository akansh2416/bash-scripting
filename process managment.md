# ⚙️ Process Management in Linux

Process management in Linux allows you to **monitor, control, and optimize running programs**. Each process has a unique **Process ID (PID)** and is typically associated with a parent process.

---

## 📘 Introduction to Process Management

A **process** is an instance of a running program. Linux provides powerful utilities to:
- View running processes
- Control execution (stop, resume, kill)
- Manage priorities
- Handle background jobs and daemons

---

## 📚 Index of Commands Covered

### 🔍 Viewing Processes
- `ps aux` – View all running processes
- `ps -u username` – View processes for a specific user
- `ps -C processname` – Show a process by name
- `pgrep processname` – Find a process by name (PID)
- `pidof processname` – Get PID of a running program

### 🔧 Managing Processes
- `kill PID` – Terminate a process by PID
- `pkill processname` – Terminate a process by name
- `kill -9 PID` – Force kill a process
- `pkill -9 processname` – Kill all instances
- `kill -STOP PID` – Stop a running process
- `kill -CONT PID` – Resume a stopped process
- `renice` – Change process priority

---

## 🔍 Viewing Processes

### Using `ps`

```bash
ps aux                # View all running processes
ps -u username        # Processes for a specific user
ps -C processname     # Show process by name
Using pgrep
bash
Copy code
pgrep processname     # Return PID(s) of process
Using pidof
bash
Copy code
pidof processname     # Find PID of a running program


🛑 Managing Processes
Killing Processes
bash
Copy code
kill PID                      # Terminate process by PID
pkill processname             # Terminate by name
kill -9 PID                   # Force kill
pkill -9 processname          # Kill all instances
⏸ Stopping & ▶️ Resuming Processes
bash
Copy code
kill -STOP PID                # Stop a process
kill -CONT PID                # Resume a stopped process


🎯 Changing Process Priority
View Priorities
bash
Copy code
top                           # Check the NI column
Change Priority
bash
Copy code
renice -n 10 -p PID           # Lower priority (positive values)
renice -n -5 -p PID           # Increase priority (root required)


🧵 Background & Foreground Processes
bash
Copy code
command &                     # Run command in background
jobs                          # List background jobs
fg %jobnumber                 # Bring job to foreground
Suspend & Resume Jobs
bash
Copy code
Ctrl + Z                      # Suspend running process
bg %jobnumber                 # Resume in background


📊 Monitoring System Processes
Using top
Interactive process viewer:

k → Kill a process (enter PID)

r → Renice a process

q → Quit

bash
Copy code
top
Using htop
A more user-friendly alternative (requires installation):

bash
Copy code
htop
✔ Supports mouse interaction
✔ Color-coded process view


⚙️ Using nice & renice
Start a Process with Priority
bash
Copy code
nice -n 10 command
Modify Existing Process Priority
bash
Copy code
renice -n -5 -p PID


🧩 Daemon Process Management
Daemon processes run in the background without user interaction.

bash
Copy code
systemctl list-units --type=service   # List all daemons
systemctl start service-name          # Start service
systemctl stop service-name           # Stop service
systemctl enable service-name         # Enable at startup


✅ Conclusion
Effective process management is critical for system performance and stability. By using tools like ps, top, htop, kill, nice, and systemctl, you gain full control over Linux processes and services.

