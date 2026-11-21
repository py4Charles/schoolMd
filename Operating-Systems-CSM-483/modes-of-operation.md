# Modes of Operation

A mechanism that allows the operating system (OS) to protect itself and other system components.

There are two modes:

- **User mode**
- **Kernel mode**

The hardware provides a **mode bit** (0 or 1), which distinguishes whether the system is running user code or kernel code.

- Some instructions are designated as **privileged instructions** and can be executed only in kernel mode.
- When a user process makes a **system call** to request a service from the OS, the system changes from user mode to kernel mode.
- When the system call completes, control returns to the user process and the mode is reset to user mode.

## Timer

To prevent a process from running in an infinite loop and consuming system resources, a **timer** is used. A timer is a hardware device.

- The timer is a counter that is decremented by the physical clock.
- It is set to generate an interrupt after a specified period.
- The operating system sets the timer counter using a privileged instruction.
- When the counter reaches zero, an interrupt is generated.
- The OS sets the timer before scheduling a process so that it can regain control or terminate a program that exceeds its allotted time.

# Process Management

A **process** is a program in execution. It is a unit of work within the system.

- A **program** is a passive entity.
- A **process** is an active entity.
- A process requires resources to accomplish its task, such as CPU, memory, I/O devices, files, and initialization data.
- When a process terminates, the OS must reclaim any reusable resources.

A **thread** is the basic unit of CPU utilization within a process.

- In a **single-threaded process**, instructions are executed sequentially, one at a time, until completion.
- The process has one program counter, which specifies the location of the next instruction to execute.
- In a **multi-threaded process**, each thread has its own program counter.
- A system usually has many processes, including user processes and operating-system processes, running concurrently on one or more CPUs.
- Concurrency is achieved by multiplexing the CPUs among the threads.

## Process Management Activities

The operating system is responsible for the following activities related to process management:

- Creating and deleting both user and system processes
- Suspending and resuming processes
- Providing mechanisms for process synchronization
- Providing mechanisms for process communication
- Providing mechanisms for deadlock handling

# Memory Management

To execute a program, all or part of its instructions and data must be in main memory.

Memory management determines what is in memory and when, in order to optimize CPU utilization and improve the computer’s response to users.

## Memory Management Activities

The operating system is responsible for:

- Keeping track of which parts of memory are currently in use and by whom
- Deciding which processes, or parts of processes, and data should be moved into and out of memory
- Allocating and deallocating memory space as needed

# Storage Management

The operating system provides a uniform, logical view of information storage.

It abstracts the physical properties of storage devices into a logical storage unit called a **file**.

Files may be stored on different storage media, including:

- Disks
- Flash memory
- Tape

Each storage medium is controlled by a **device driver**, such as a disk drive or tape drive.

Storage devices vary in properties such as:

- Access speed
- Capacity
- Data-transfer rate
- Access method, such as sequential or random access

# File-System Management

Files are usually organized into **directories**.

Most systems provide access control to determine which users can access which files.

## File-System Management Activities

The operating system is responsible for:

- Creating and deleting files and directories
- Providing primitives to manipulate files and directories
- Mapping files onto secondary storage
- Backing up files onto stable, non-volatile storage media

# Secondary-Storage Management

Secondary storage, usually disks, is used to store data that does not fit in main memory or data that must be kept for a long period of time.

Proper management of secondary storage is important because the overall speed of a computer can depend heavily on the disk subsystem and its algorithms.

## Secondary-Storage Management Activities

The operating system is responsible for:

- Free-space management
- Storage allocation
- Disk scheduling

Some storage does not need to be fast. **Tertiary storage** includes optical storage and magnetic tape, but it still must be managed by the operating system or applications.

# Caching

Caching is an important principle performed at many levels in a computer, including hardware, the operating system, and software.

Information currently in use is copied temporarily from slower storage to faster storage.

- The faster storage, called the **cache**, is checked first.
- If the required information is in the cache, it is used directly.
- If it is not in the cache, the data is copied from the slower storage into the cache and then used.
- A cache is smaller in size than the storage it caches.
- Cache management is an important design problem, especially regarding cache size and replacement policy.

## Data Migration

When data “A” is migrated from disk to a register, the system must ensure that the most recent value is used, regardless of where it is stored in the storage hierarchy.

- In a **multitasking environment**, the OS must be careful to use the most recent value of data.
- In a **multiprocessor environment**, hardware must provide cache coherency so that all CPUs have the most recent value in their caches.
- In a **distributed environment**, the situation is more complex because several copies of the same data may exist.
- Various solutions to this problem are covered in Chapter 17.

# I/O Subsystem

One purpose of an operating system is to hide the peculiarities of hardware devices from users.

The **I/O subsystem** is responsible for:

- Managing I/O memory, including buffering, caching, and spooling
- Providing a general device-driver interface
- Providing drivers for specific hardware devices

## I/O Concepts

- **Buffering:** Temporarily storing data while it is being transferred.
- **Caching:** Storing parts of data in faster storage to improve performance.
- **Spooling:** Overlapping the output of one job with the input of other jobs.