# Computer System Organization, Interrupts, and Storage

## Modern General-Purpose Computer System

A modern general-purpose computer system consists of:

- One or more CPUs
- A number of device controllers
- A common bus that provides access to shared memory

Each **device controller** is in charge of a specific type of device, such as:

- Disk drives
- Audio devices
- Video displays

Each device controller has a **local buffer**.

The CPU moves data:

- From main memory to local buffers
- From local buffers to main memory

The CPU and device controllers can execute in parallel, competing for memory cycles. To ensure orderly access to shared memory, a **memory controller** synchronizes access to memory.

## Bootstrap Program

A **bootstrap program** is loaded at power-up or reboot.

- Typically stored in ROM or EPROM, generally known as **firmware**
- Initializes all aspects of the system
- Loads the operating system kernel and starts execution

Once the kernel is loaded and executing, it can start providing services to the system and its users.

Some services are provided outside the kernel by **system programs** that are loaded into memory at boot time. These become:

- **System processes**
- **System daemons** that run the entire time the kernel is running

On UNIX, the first system process is **init**, and it starts many other daemons. Once this phase is complete, the system is fully booted and waits for an event to occur.

## Interrupts

The occurrence of an event is usually signaled by an **interrupt**.

There are two types of interrupts:

| Type | Description |
|---|---|
| **Hardware interrupt** | A device may trigger an interrupt by sending a signal to the CPU, usually by way of the system bus. |
| **Software interrupt** | A program may trigger an interrupt by executing a special operation called a **system call**. |

A software-generated interrupt is sometimes called a **trap** or **exception**. It is caused either by:

- An error, such as divide by zero
- A user request, such as an I/O request

An operating system is **interrupt driven**.

## Interrupt Handling

When an interrupt occurs, the operating system:

1. Preserves the state of the CPU by storing the registers and the program counter.
2. Determines which type of interrupt has occurred.
3. Transfers control to the interrupt-service routine.

An **interrupt-service routine** is a collection of routines or modules. Each module is responsible for handling one particular interrupt, such as an interrupt from:

- A printer
- A disk

The transfer is generally made through the **interrupt vector**, which contains the addresses of all the service routines.

Interrupt architecture must save the address of the interrupted instruction.

## Interrupt-Driven I/O Cycle

1. **Device Driver Initiates I/O**  
   The CPU, via an OS device driver, executes instructions to request an I/O operation, such as reading data from disk or receiving network packets.

2. **Command to Controller**  
   The device driver sends commands or data requests directly to the I/O controller.

3. **Hardware Execution**  
   The I/O controller initiates and performs the physical hardware operation independently.  
   While the I/O controller works in parallel, the CPU continues executing normal instructions, checking for interrupt signals after every instruction cycle.

4. **Signal Generation**  
   Once input is ready, output is complete, or an error occurs, the I/O controller generates an explicit interrupt signal back to the CPU hardware.

5. **Control Transfer and Handler Processing**  
   Upon receiving the interrupt, the CPU pauses its current task and transfers control to the appropriate interrupt handler routine.  
   The interrupt handler processes the data, for example by moving bytes into memory, and issues a return command.

6. **Task Resumption**  
   The CPU restores the state of the interrupted program and resumes processing the original task from where it was paused.

7. **Loop Back**  
   The driver or process resumes normal operation, ready to initiate the next I/O cycle whenever required.

## Storage Structure

### Main Memory

- The only large storage media that the CPU can access directly
- Random access
- Typically volatile

### Secondary Storage

Secondary storage is an extension of main memory that provides large nonvolatile storage capacity.

#### Hard Disks

- Rigid metal or glass platters covered with magnetic recording material
- The disk surface is logically divided into **tracks**, which are subdivided into **sectors**
- The disk controller determines the logical interaction between the device and the computer

#### Solid-State Disks

- Faster than hard disks
- Nonvolatile
- Based on various technologies
- Becoming more popular

## Basic Units of Computer Storage

The basic unit of computer storage is the **bit**. A bit can contain one of two values: 0 and 1. All other storage in a computer is based on collections of bits.

- A **byte** is 8 bits, and on most computers it is the smallest convenient chunk of storage.
- A less common term is **word**, which is a given computer architecture’s native unit of data. A word is made up of one or more bytes.

Computer storage, along with most computer throughput, is generally measured and manipulated in bytes and collections of bytes.

| Unit | Size |
|---|---|
| Kilobyte (KB) | 1,024 bytes |
| Megabyte (MB) | \(1,024^2\) bytes |
| Gigabyte (GB) | \(1,024^3\) bytes |
| Terabyte (TB) | \(1,024^4\) bytes |
| Petabyte (PB) | \(1,024^5\) bytes |

Additional units include:

- Exabyte
- Zettabyte
- Yottabyte

Computer manufacturers often round off these numbers and say that a megabyte is 1 million bytes and a gigabyte is 1 billion bytes.

Networking measurements are an exception to this general rule. They are given in **bits**, because networks move data a bit at a time.

## Caching

**Caching** is copying information from “slow” storage into a faster storage system.

- Main memory can be viewed as a cache for secondary storage.
- A **device driver** is provided for each device controller to manage I/O.
- The device driver provides a uniform interface between the controller and the kernel.