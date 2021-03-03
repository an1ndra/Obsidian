
## `ris:Computer` Computer Organization
1. Explain IEEE single precision formats for representing -10.5
2. Explain “`write back`” and “`write through`” policies in cache memory.
	
	|Write Through|Write Black|
	|--------------|------------|
	|Main memory always contains same data as cache.|Main memory and cache memory may have different data.|
	|Number of memory write operation in a typical program is more.| Number of memory write operation in a typical program is less|
	|When I/O device communicated through DMA would receive most recent data.|When I/O device communicated through DMA would not receive most recent data.|
	|It is a process of writing cache and main memory simultaneously.|It is a process of writing cache and data is removed from cache, first copied to main memory.|
	
	
3. Why is DMA mode of data transfer used? Explain briefly.
	**Direct memory access (DMA) is a method that allows an input/output (I/O) device to send or receive data directly to or from the main memory, bypassing the CPU to speed up memory operations**
	Without DMA, when the CPU is using [programmed input/output](https://en.wikipedia.org/wiki/Programmed_input/output "Programmed input/output"), it is typically fully occupied for the entire duration of the read or write operation, and is thus unavailable to perform other work. With DMA, the CPU first initiates the transfer, then it does other operations while the transfer is in progress, and it finally receives an [interrupt](https://en.wikipedia.org/wiki/Interrupt "Interrupt") from the DMA controller (DMAC) when the operation is done. 
	This feature is useful at any time that the CPU cannot keep up with the rate of data transfer, or when the CPU needs to perform work while waiting for a relatively slow I/O data transfer. Many hardware systems use DMA, including [disk drive](https://en.wikipedia.org/wiki/Disk_storage "Disk storage") controllers, [graphics cards](https://en.wikipedia.org/wiki/Video_card "Video card"), [network cards](https://en.wikipedia.org/wiki/Network_interface_controller "Network interface controller") and [sound cards](https://en.wikipedia.org/wiki/Sound_card "Sound card"). DMA is also used for intra-chip data transfer in [multi-core processors](https://en.wikipedia.org/wiki/Multi-core_processor "Multi-core processor"). Computers that have DMA channels can transfer data to and from devices with much less CPU overhead than computers without DMA channels. Similarly, a [processing element](https://en.wikipedia.org/wiki/Processing_element "Processing element") inside a multi-core processor can transfer data to and from its local memory without occupying its processor time, allowing computation and data transfer to proceed in parallel.
	
4. Compare and contrast CISC and RISC.
 
	comparison|RISC|CISC
	--------|--------|------
	Emphasis on|Software|Hardware
	Includes|Single clock|Multi-clock
	Instruction-set size|Small|Large
	Instruction|fixed (32-bit) format|Varying formats (16-64 bits each instruction)
	Addressing modes used|Limited to 3-5|12-24
	General purpose registers used|32-192|8-24
	Memory inferences|Register to register|Memory to memory
	Cache design|Split data cache and instruction cache.|Unified cache for instructions and data.
	Clock rate|50-150 MHz|33-50 MHz
	CPU Control|Hardwired without control memory.|Micro-coded using control memory (ROM).
	
5. What is virtual memory? Explain virtual and logical address space.
	![](https://upload.wikimedia.org/wikipedia/commons/thumb/6/6e/Virtual_memory.svg/250px-Virtual_memory.svg.png)
	**Virtual memory** is a method of using the computer [hard drive](https://www.computerhope.com/jargon/h/harddriv.htm) to provide extra [memory](https://www.computerhope.com/jargon/m/memory.htm) for the computer. Segments of memory are stored on the hard drive known as pages. When a segment of memory is requested that is stored in virtual memory, it is loaded into the actual memory address.
	
	**virtual address space (VAS):** In [computing](https://en.wikipedia.org/wiki/Computing "Computing"), a virtual address space (VAS) or address space is the set of ranges of virtual addresses that an [operating system](https://en.wikipedia.org/wiki/Operating_system "Operating system") makes available to a process.[\[1\]](https://en.wikipedia.org/wiki/Virtual_address_space#cite_note-1) The range of virtual addresses usually starts at a low address and can extend to the highest address allowed by the computer's [instruction set architecture](https://en.wikipedia.org/wiki/Instruction_set "Instruction set") and supported by the [operating system](https://en.wikipedia.org/wiki/Operating_system "Operating system")'s pointer size implementation, which can be 4 [bytes](https://en.wikipedia.org/wiki/Bytes "Bytes") for [32-bit](https://en.wikipedia.org/wiki/32-bit "32-bit") or 8 [bytes](https://en.wikipedia.org/wiki/Bytes "Bytes") for [64-bit](https://en.wikipedia.org/wiki/64-bit "64-bit") OS versions. This provides several benefits, one of which is security through [process isolation](https://en.wikipedia.org/wiki/Process_isolation "Process isolation") assuming each process is given a separate [address space](https://en.wikipedia.org/wiki/Address_space "Address space").
	
	**Logical Address space (LAS):** is generated by CPU while a program is running. The logical address is virtual address as it does not exist physically, therefore, it is also known as Virtual Address. This address is used as a reference to access the physical memory location by CPU. The term Logical Address Space is used for the set of all logical addresses generated by a program’s perspective.  
	The hardware device called Memory-Management Unit is used for mapping logical address to its corresponding physical address.
	
6. Design the flowchart of restoring and non restoring division algorithm.
<br>
	![enter image description here](https://i.imgur.com/84RILcQ.png)
<br>
![enter image description here](https://i.imgur.com/MLWLkIU.png)
## `ris:Questionnaire` BIg answer type question
8. What do you mean by memory –mapped I/O and I/O- mapped I/O? Design and describe a 4-bit ALU and its operation.
 **Memory Mapped I/O –**
In this case every bus in common due to which the same set of instructions work for memory and I/O. Hence we manipulate I/O same as memory and both have same address space, due to which addressing capability of memory become less because.
![](https://media.geeksforgeeks.org/wp-content/uploads/Untitled-drawing-2-1.png)

Arithmetic and Logic Unit (ALU) is made of Arithmetic and Logic Units. This paper considers and designed sub-blocks such as Adder/subtraction block, 4-bit multiplier, Magnitude Comparator and Multiplexers using Proteus.

![[Pasted image 20210303141828.png]]
9. Explain different types of DMA controller and how do they differ to each other? Explain with example `Belady’s `anomaly for page replacement policy. Evaluate the following expression using 0,1,2,3 address instruction: Y = ( A + B ) x ( C – D ).

The DMA controller transfers the data in three modes:
	- **Burst Mode:** Here, once the DMA controller gains the charge of the system bus, then it releases the system bus only after **completion** of data transfer. Till then the CPU has to wait for the system buses.
	- **Cycle Stealing Mode:** In this mode, the DMA controller **forces** the CPU to stop its operation and **relinquish the control over the bus** for a **short term** to DMA controller. After the **transfer of every byte**, the DMA controller
	**releases** the **bus** and then again requests for the system bus. In this way, the DMA controller steals the clock cycle for transferring every byte.
	- **Transparent Mode:** Here, the DMA controller takes the charge of system bus only if the **processor does not require the system bus**.
	
	**Example:** Consider the following diagram to understand the behaviour of a stack-based page replacement algorithm

![](https://media.geeksforgeeks.org/wp-content/uploads/stackbased.png)

The diagram illustrates that given the set of pages i.e. {0, 1, 2} in 3 frames of memory is not a subset of the pages in memory – {0, 1, 4, 5} with 4 frames and it is a violation in the property of stack based algorithms. This situation can be frequently seen in FIFO algorithm.

**Belady’s Anomaly in FIFO –**  
Assuming a system that has no pages loaded in the memory and uses the FIFO Page replacement algorithm. Consider the following reference string:

> 1, 2, 3, 4, 1, 2, 5, 1, 2, 3, 4, 5 

**Case-1:** If the system has 3 frames, the given reference string on using FIFO page replacement algorithm yields a total of 9 page faults. The diagram below illustrates the pattern of the page faults occurring in the example.

![](https://media.geeksforgeeks.org/wp-content/uploads/fifo3.png)

**Case-2:** If the system has 4 frames, the given reference string on using FIFO page replacement algorithm yields a total of 10 page faults. The diagram below illustrates the pattern of the page faults occurring in the example.

![](https://media.geeksforgeeks.org/wp-content/uploads/fifo4.png)

It can be seen from the above example that on increasing the number of frames while using the FIFO page replacement algorithm, the number of **page faults increased** from 9 to 10.


10. Distinguish between SRAM and DRAM. Design the bus connection with a CPU to contact four RAM chips of size 256 x 8 bits each and a ROM chip of 512 x 8 bit size. Assume that CPU has 8-bit data bus and 16-bit address bus.
11. Write short notes on any three of the following:

	a) Cache replacement policy
		In computing, cache algorithms are optimizing instructions, or algorithms, that a computer program or a hardware-maintained structure can utilize in order to manage a cache of information stored on the computer.
	
	b) Flynn’s Classification
		Flynn's taxonomy is a classification of computer architectures, proposed by Michael J. Flynn in 1966. The classification system has stuck, and it has been used as a tool in design of modern processors and their functionalities. Since the rise of multiprocessing central processing units, a multiprogramming context has evolved as an extension of the classification system.
	
	c) Bus organization
		Bus is a group of conducting wires which carries information, all the peripherals are connected to microprocessor through Bus.
		f) Different hazards in pipe-lining
	