# KernelLite 🧠⚙️  
*A Lightweight Multi-Process CPU Scheduler Simulator in C*

**KernelLite** is a simplified simulation of a UNIX-like operating system scheduler that demonstrates how modern CPU scheduling works under the hood. It includes a custom shell to manage process submissions and a daemon scheduler that executes user jobs using Round-Robin and Priority-based scheduling across limited CPU resources.

> 🔧 Built entirely in **C** using low-level Linux system programming — with real process forking, signal handling, and process control.

---

## 🚀 Features

- ⚙️ **Round-Robin Scheduling** with configurable CPU time slice (`TSLICE`)
- ⭐ **Fixed-Priority Scheduling** (Levels 1–4) with user-defined priorities
- 🔁 Preemptive multitasking simulation using signals and timers
- 💡 Shell interface (`SimpleShell`) for submitting jobs at runtime
- 🧠 Smart daemon scheduler that manages the ready and running queues
- 📊 Execution & wait time tracking for each job
- ❌ Blocks submission of jobs with blocking system calls (`scanf`, `sleep`, etc.)
- 👋 Graceful shutdown with summary stats for all jobs

---

## 🧪 How to Use

### 1. Compile the Shell and Scheduler
```bash
gcc SimpleShell.c -o SimpleShell
```
### 2.Run the Shell with Arguments
```bash
./SimpleShell <NCPU> <TSLICE_in_ms>
```
### 3.Submit a Job via the Shell
```bash
SimpleShell$ submit ./a.out 3
```
