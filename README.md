# Customized Virtual File System (CVFS)

A **Customized Virtual File System (CVFS)** implemented in **C** to understand the internal working of file systems and important Operating System concepts.

The project simulates components such as **Boot Block, Super Block, Inodes, File Table, UAREA, UFDT, file descriptors, file permissions, and file offsets**.

## Features

* Create regular files
* Read and write file data
* Display file information using `stat`
* List files using `ls` and `ls -a`
* Delete files using `unlink`
* Change file read offset using `lseek`
* File permission handling
* Inode and file descriptor management
* Backup CVFS files to the host file system
* Command-line interface

## Commands

```text
help
man <command>
clear
ls
ls -a
creat <filename> <permission>
write <fd>
read <fd> <size>
stat <filename>
lseek <fd> <offset> <whence>
unlink <filename>
exit
```

## Architecture

```text
CVFS
 |
 +-- Boot Block
 +-- Super Block
 +-- DILB / Inode Linked List
 +-- UAREA
      |
      +-- UFDT
           |
           +-- File Table
                |
                +-- Inode
                     |
                     +-- Data Buffer
```

## Technologies Used

* **Language:** C
* **Interface:** Command Line
* **Data Structure:** Linked List
* **Concepts:** Operating Systems, File Systems, File Handling, Dynamic Memory Allocation

The project uses standard C/POSIX headers such as `stdio.h`, `stdlib.h`, `unistd.h`, `fcntl.h`, `string.h`, and `stdbool.h`.

## Configuration

```c
MAXINODE       = 5
MAXFILESIZE    = 50 bytes
MAXOPENFILES   = 5
```

## How to Run

### Linux / WSL

```bash
gcc CVFS.c -o Myexe
./Myexe
```

### Windows with GCC/MinGW

```bash
gcc CVFS.c -o Myexe.exe
Myexe.exe
```

## Learning Outcomes

This project helps understand:

* File System Architecture
* Inodes and Super Block
* UAREA and UFDT
* File Tables and File Descriptors
* File Permissions
* Read/Write Operations
* File Offsets
* Dynamic Memory Allocation
* Linked Lists

## Author

**Shreya Vilas Kulkarni**

> An educational implementation of a customized Virtual File System developed in C to demonstrate core Operating System and File System concepts.
