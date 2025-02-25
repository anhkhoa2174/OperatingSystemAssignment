# Simple Operating System Simulation

## Project Overview

This project simulates a basic operating system to help understand key concepts in OS design, such as **scheduler**, **synchronization**, and **memory management**. The OS manages two primary resources: **CPU** and **RAM**, with the goal of allowing multiple processes to run concurrently.

Key modules implemented:
1. **Scheduler**:
   - Uses the **Multi-Level Queue (MLQ)** scheduling algorithm, which assigns processes to different queues based on their priority.
   - The scheduler assigns time slices for each process to run on the CPU.

2. **Synchronization**:
   - Implements mechanisms to prevent race conditions and ensure the safe access to shared resources by multiple processes.

3. **Memory Management**:
   - Focuses on **paging-based memory management**, including virtual-to-physical memory mapping.
   - **Translation Lookaside Buffer (TLB)** is used to optimize access time for memory address translation.
   - Implements memory allocation, deallocation, and swapping between physical memory and swap space.

## Project Components
1. **Scheduler**:
   - **MLQ Policy**: Processes are grouped by priority into multiple queues. The CPU scheduler picks processes from these queues in a round-robin fashion, ensuring that higher-priority processes get CPU time more often.
   
2. **Memory Management**:
   - Implements a **paging-based address translation** scheme, mapping virtual addresses to physical frames.
   - Each process has its own **page table** and **virtual memory mapping**.
   - **TLB (Translation Lookaside Buffer)** is used to optimize memory access times by caching recent page table entries.

3. **Implementation Details**:
   - The system manages processes through **process control blocks (PCB)**, which include the process's priority, registers, and memory mappings.
   - Processes can perform operations such as **calculation**, **memory allocation (alloc)**, **memory deallocation (free)**, and **memory read/write**.
   - The OS uses a simple **round-robin scheduling** for process execution within each queue.

4. **How to Run the Simulation**:
   - The simulation is executed by running the `./os [configure_file]` command, where the configuration file specifies the number of CPUs, processes, and memory settings.
   - The program simulates the OS's behavior based on the configuration, including the scheduling of processes and memory operations.

5. **Additional Features**:
   - The OS supports **paging**, **TLB operations**, and **swapping** between RAM and secondary memory (SWAP).
   - **Synchronization** mechanisms are used to ensure safe concurrent access to shared resources by multiple processes.

## How to Build
1. Compile the source code with the `make all` command.
2. Run the simulation using `./os [configure_file]` where `[configure_file]` specifies the configuration settings for CPU, memory, and processes.

## Result
The project helps simulate the basic operations of an operating system, providing an understanding of key OS components such as process scheduling, memory management, and synchronization mechanisms.
