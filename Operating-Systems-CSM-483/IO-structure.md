# Computer-System Architecture

A general-purpose computer system consists of CPUs and multiple device controllers connected through a common bus.

- Each device controller is in charge of a specific type of device.
- More than one device may be attached to a controller. For example, seven or more devices can be attached to a Small Computer Systems Interface (SCSI) controller.
- A device controller maintains some local buffer storage and a set of special-purpose registers.
- The device controller is responsible for moving data between the peripheral devices it controls and its local buffer storage.
- Typically, operating systems have a device driver for each device controller. The device driver understands the device controller and provides the rest of the operating system with a uniform interface to the device.

## I/O Operation

To start an I/O operation:

1. The device driver loads the appropriate registers within the device controller.
2. The device controller examines the contents of these registers to determine what action to take, such as reading a character from the keyboard.
3. The controller starts transferring data from the device to its local buffer.
4. Once the transfer is complete, the device controller informs the device driver through an interrupt that the operation has finished.
5. The device driver then returns control to the operating system, possibly returning the data or a pointer to the data if the operation was a read.
6. For other operations, the device driver returns status information.

## Interrupt-Driven I/O

Interrupt-driven I/O is suitable for moving small amounts of data, but it can create high overhead when used for bulk data movement, such as disk I/O.

To solve this problem, **Direct Memory Access (DMA)** is used.

- After setting up buffers, pointers, and counters for the I/O device, the device controller transfers an entire block of data directly between its own buffer storage and memory.
- This occurs without intervention from the CPU.
- Only one interrupt is generated per block, to tell the device driver that the operation has completed.
- While the device controller performs these operations, the CPU is available to accomplish other work.

Some high-end systems use a **switch** rather than a bus architecture. On these systems, multiple components can communicate with other components concurrently rather than competing for cycles on a shared bus. In this case, DMA is even more effective.

# Multiprocessor Systems

## Single and Multiple Processors

- Most systems have a single general-purpose processor.
- Many systems also include special-purpose processors.
- Multiprocessor systems are growing in use and importance.
- Multiprocessor systems are also known as **parallel systems** or **tightly coupled systems**.

## Advantages

Multiprocessor systems provide several advantages:

- Increased throughput
- Economy of scale
- Increased reliability through graceful degradation and fault tolerance

## Types of Multiprocessing

| Type | Description |
|---|---|
| Symmetric Multiprocessing (SMP) | Each processor performs all tasks |
| Asymmetric Multiprocessing | Each processor is assigned a specific task |

# Multicore Systems

Most modern CPU designs include multiple computing cores on a single chip. Such multiprocessor systems are called **multicore systems**.

Multicore systems can be more efficient than multiple single-core chips because:

- On-chip communication is faster than communication between separate chips.
- One chip with multiple cores uses significantly less power than multiple single-core chips.
- Lower power consumption is especially important for laptops and mobile devices.

> **Note:** While multicore systems are multiprocessor systems, not all multiprocessor systems are multicore.

# Clustered Systems

Clustered systems are like multiprocessor systems, except that multiple complete computer systems work together.

- They usually share storage through a **Storage-Area Network (SAN)**.
- They provide high-availability services that can survive failures.

## Types of Clustering

- **Asymmetric clustering:** One machine operates in hot-standby mode.
- **Symmetric clustering:** Multiple nodes run applications and monitor one another.

Some clusters are designed for **high-performance computing (HPC)**. Applications must be written to use parallelization. Some clusters also use a **Distributed Lock Manager (DLM)** to avoid conflicting operations.

# Multiprogrammed Systems

A single user cannot keep both the CPU and I/O devices busy at all times.

**Multiprogramming** organizes jobs, consisting of code and data, so that the CPU always has at least one job to execute.

- A subset of the total jobs in the system is kept in memory.
- In **batch systems**, one job is selected and run through job scheduling.
- When a job must wait, for example for I/O, the operating system switches to another job.
- **Timesharing systems** are a logical extension of batch systems.
- In timesharing, the CPU switches between jobs so frequently that users can interact with each job while it is running, creating interactive computing.