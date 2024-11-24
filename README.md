
# Enhanced xv6 Kernel with System Call Extensions

This project enhances the xv6 operating system kernel by adding several new system calls and commands for improved functionality. These additions include:

1. **Message Passing (`send` and `recv` system calls)**.
2. **Retrieve Parent Process ID (`getppid` system call)**.
3. **Process Listing (`ps` command)**.
4. **File Copying (`copy` system call)**.

---

## Detailed Documentation

The README contains full details of each modification made to the kernel, including:

### 1. Message Passing (`send` and `recv`)
- **Implemented System Calls**:
  - `send(type, message)`
  - `recv(type, buffer)`
- Modifications included changes in `syscall.h`, `syscall.c`, `usys.S`, `user.h`, and a test case program to validate the implementation.

### 2. `getppid` (Parent Process ID Retrieval)
- Added `getppid` as a new system call to retrieve the parent process ID.
- Detailed kernel-level changes and user-space usage are provided.

### 3. Process Listing (`ps`)
- Added a `ps` command to list all processes with their details.
- Modifications spanned across the process table and user interface.

### 4. File Copying (`copy`)
- Introduced a new `copy` system call for file duplication at the kernel level.
- Includes implementation details, edge-case handling, and testing instructions.

---

## Building the Kernel

1. **Clean and Build**:
   ```bash
   make clean
   make
   ```

2. **Run in QEMU**:
   ```bash
   make qemu
   ```

## Testing

- Each functionality is tested with dedicated user-level programs provided in the repository.
- Follow the test instructions for `msg_test.c`, `ppid_test.c`, and manual commands like `ps` and `copy`.

## File Modifications

All kernel-level changes, including code snippets and explanations, are documented in the README for each modified file.

---

This README file serves as a detailed guide for developers to understand the enhancements made to the xv6 kernel.
