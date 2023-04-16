## Operating System Concepts

### Chapter 9: Main Memory
* **9.1.1 Basic Hardware**
	* Main memory and registers are the only general-storage the CPU can access.
	* Registers are generally available within 1 cycle of the CPU clock.
	* We must protect the operating system from access by user processes, as well as
	  protect user processes from one another. (This protection has to be implemented
	  by the hardware because the OS does not usually intervene between the CPU and it's
	  memory accesses.)
	* To achieve this, we need to ensure that each process has a separate memory space.
	  To do so, we need to determine the range of addresses that the process may access.
	  This is done by using two registers: a *base*, and a *limit*. *limit* specifies the
	  size of the range. (Manipulating these registers can only be done in kernel mode.)
* **9.1.2 Address Binding**
	* Addresses in source programs are generally symbolic. A compiler *binds* these addresses
	  to relocatable addresses. (such as "14 bytes from the beginning of this module")
	* The linker in turn binds the relocatable addresses to absolute addresses.
	* CPU (Logical address) -> Memory management unit (Physical address) -> Physical memory
	* The logical address is usually referred to as *virtual address*.
* **9.2.2 Memory Allocation**
	* First fit: Allocate the first hole that is big enough.
	* Best fit: Allocate the *smallest* hole that is big enough. Produces *smallest* leftover hole.
	* Worst fit: Allocate the largest hole. Produces *largest* leftover hole.
	* Simulations have shown that first fit and best fit are better than worst fit for decreasing
	  time and storage utilization.
	* Neither first fit or best fit are better than the other, but first fit is generally faster.
	* *First fit* and *best fit* both suffer from *external* memory fragmentation. As processes are
	  loaded and removed, the free memory space is broken into little pieces.
	* *External fragmentation*: There is enough total memory space to satisfy a request but the available
	  spaces are not contiguous: storage is fragmented into a large number of small holes.
	* A solution to external fragmentation is called *paging*, this is the concept of permitting
	  the logical address space of processes to be noncontiguous.
* **9.3.1 Basic Paging Method**
