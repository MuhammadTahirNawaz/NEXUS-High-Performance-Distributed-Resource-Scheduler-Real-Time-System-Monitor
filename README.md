# NEXUS: High-Performance Distributed Resource Scheduler

The NEXUS OS Scheduler is a real-time process scheduling simulator designed to demonstrate core operating system concepts through practical implementation. The system uses a true multi-process architecture and System V Inter-Process Communication (IPC), including shared memory and message queues, to emulate how an operating system schedules and manages processes across multiple CPU cores.

---

### Key Features

* **Real-Time TUI Dashboard**: Displays job queue, worker status, system logs, and statistics using an ncurses interface.
* **Master-Worker Architecture**: A Master process acts as the kernel scheduler while multiple Worker processes simulate CPU cores.
* **Inter-Process Communication**: Uses Shared Memory for status tracking and Message Queues for job dispatching.
* **Scheduling Policy**: Implements priority-based queuing (High, Medium, Low) combined with round-robin dispatch.
* **Synchronization**: Utilizes POSIX mutexes with PTHREAD_PROCESS_SHARED to prevent race conditions in shared memory.
* **Heartbeat Monitoring**: Detects scheduler failure through periodic timestamp updates.
* **Graceful Shutdown**: Handles SIGINT by terminating workers safely and cleaning up IPC resources.

---

### System Design

* **Master Process**: Initializes IPC resources, generates/dispatches jobs, and manages scheduling.
* **Worker Processes**: Receive jobs via message queues, execute tasks (burst times 1-10s), and update progress.
* **UI Process**: Attaches to shared memory in read-only mode to visualize system state.

---

### Group Members

* **ZAIN IQBAL** (2023-CS-614)
* **MOHSIN ALI** (2023-CS-631)
* **TAHIR NAWAZ** (2023-CS-633)

**Department**: DEPARTMENT OF COMPUTER SCIENCE, UET LAHORE (NEW CAMPUS, KSK)
