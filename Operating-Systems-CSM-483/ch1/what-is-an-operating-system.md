# What is an Operating System?

A program that acts as an intermediary between a user of a computer and the computer hardware.

## Operating System Goals

- Execute user programs and make solving user problems easier
- Make the computer system convenient to use
- Use the computer hardware in an efficient manner

## Four Components of a Computer System

A computer system can be divided into four components:

1. **Hardware** – provides basic computing resources
   - CPU, memory, I/O devices

2. **Operating system**
   - Controls and coordinates use of hardware among various applications and users

3. **Application programs** – define the ways in which the system resources are used to solve the computing problems of the users
   - Word processors, compilers, web browsers, database systems, video games

4. **Users**
   - People, machines, other computers

## User Views of the Computer

The user's view of the computer varies according to the interface being used:

- **Single-user computers** (e.g., PC, workstations)
  - Such systems are designed for one user to monopolize its resources.
  - The goal is to maximize the work (or play) that the user is performing.
  - The operating system is designed mostly for ease of use and good performance.

- **Multi-user computers** (e.g., mainframes, computing servers)
  - These users share resources and may exchange information.
  - The operating system in such cases is designed to maximize resource utilization — to assure that all available CPU time, memory, and I/O are used efficiently and that no individual user takes more than their fair share.

- **Handheld computers** (e.g., smartphones and tablets)
  - The user interface for mobile computers generally features a touch screen.
  - The systems are resource poor, optimized for usability and battery life.

- **Embedded computers** (e.g., computers in home devices and automobiles)
  - The user interface may have numeric keypads and may turn indicator lights on or off to show status.
  - The operating systems are designed primarily to run without user intervention.

## The Computer's Point of View

From the computer's point of view, the operating system is the program most intimately involved with the hardware. There are two different views:

- **The operating system is a resource allocator**
  - Manages all resources
  - Decides between conflicting requests for efficient and fair resource use

- **The operating system is a control program**
  - Controls execution of programs to prevent errors and improper use of the computer

## Common Definition

A more common definition, and the one that we usually follow, is that the operating system is the one program running at all times on the computer — usually called the **kernel**.

Along with the kernel, there are two other types of programs:

- **System programs**, which are associated with the operating system but are not necessarily part of the kernel.
- **Application programs**, which include all programs not associated with the operation of the system.

## Mobile Operating Systems

Mobile operating systems often include not only a core kernel but also **middleware** — a set of software frameworks that provide additional services to application developers.