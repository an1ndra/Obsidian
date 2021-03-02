# Assignment

1. Answer the following:
a) Briefly discuss the Von-Neumann architecture of digital computer. Compare and contrast
the Harvard architecture with Von-Neumann architecture. 3+2

    Von Neumann architecture is an early, influential type of computing structure. It primarily consists of memory chips that are able to both hold and process data. Each chip has the ability to perform different tasks, depending on how it is affected by the operation executed before it. In this architecture, each computer would have memory, mechanisms for output and input, a central control, a place for central arithmetic, and external storage.

    Computers with Von Neumann architecture are known as stored-program. This means that the computer does not need external switches or other influences in order to run. All instructions and data are stored in random-access memory (RAM).

    Before the Von Neumann system, computers were essentially designed rather than being programmed. Once a machine was assembled, it could only perform one function. In order to change what the computer did, it was necessary to rewire, add components, or otherwise alter the physical structure of the machine.

    ![Assignment%20cf52ee630c9447cd8d664ae6b6e23ad8/Von-Neumann-Architecture-VERSUS-Harvard-Architecture.jpg](Assignment%20cf52ee630c9447cd8d664ae6b6e23ad8/Von-Neumann-Architecture-VERSUS-Harvard-Architecture.jpg)

b) Briefly explain IEEE 754 standard for floating point representation in single precision.
Represent (-7.25)10 in IEEE 754 single precision format. 2+3

[Single-precision floating-point format](https://en.wikipedia.org/wiki/Single-precision_floating-point_format#Converting_from_decimal_representation_to_binary32_format)

[](https://www.geeksforgeeks.org/ieee-standard-754-floating-point-numbers/)

[https://www.youtube.com/watch?v=atlaD7M30sY](https://www.youtube.com/watch?v=atlaD7M30sY)

c) What do you mean by Computer Organization? How it related with Computer
Architecture? 3+2

Computer organization refers to the operational units and their interconnections that realize the architectural specifications. Examples of architectural attributes include the instruction set, the number of bits used to represent various data types (e.g., numbers, characters), I/O mechanisms, and techniques for addressing memory. Organizational attributes include those hardware details transparent to the programmer, such as control signals; interfaces between the computer and peripherals; and the memory technology used.

d) Explain Associative Memory. Discuss the advantages over Secondary Memory.3+2

An associative memory can be considered as a memory unit whose stored
 data can be identified for access by the content of the data itself 
rather than by an address or memory location.

Associative memory is often referred to as **Content Addressable Memory (CAM)**.

When a write operation is performed on associative memory, no address
 or memory location is given to the word. The memory itself is capable 
of finding an empty unused location to store the word.

On the other hand, when the word is to be read from an associative 
memory, the content of the word, or part of the word, is specified. The 
words which match the specified content are located by the memory and 
are marked for reading.

The following diagram shows the block representation of an Associative memory.

![https://static.javatpoint.com/tutorial/coa/images/coa-associative-memory.png](https://static.javatpoint.com/tutorial/coa/images/coa-associative-memory.png)

From the block diagram, we can say that an associative memory 
consists of a memory array and logic for 'm' words with 'n' bits per 
word.

The functional registers like the argument register **A** and key register **K** each have **n** bits, one for each bit of a word. The match register **M** consists of **m** bits, one for each memory word.

The words which are kept in the memory are compared in parallel with the content of the argument register.

The key register (K) provides a mask for choosing a particular field 
or key in the argument word. If the key register contains a binary value
 of all 1's, then the entire argument is compared with each memory word.
 Otherwise, only those bits in the argument that have 1's in their 
corresponding position of the key register are compared. Thus, the key 
provides a mask for identifying a piece of information which specifies 
how the reference to memory is made.

The following diagram can represent the relation between the memory array and the external registers in an associative memory.

1. Compared to main memory, secondary memory is slower, bigger,
cheaper (per unit storage).

2. The capacity of secondary storage is between 10 to 250
GB.

3. Data stored in secondary storage devices is permanent (non
volatile) in nature.

Answer the following:
a) Explain Booth’s multiplication algorithm with a suitable flowchart. Multiply (+14) with
(-5) using Booth’s algorithm. 7+8

[https://www.youtube.com/watch?v=DIp4GqSCZho](https://www.youtube.com/watch?v=DIp4GqSCZho)

b) What is memory mapping? Explain Set associative mapping using an example. Explain
Locality of reference. Draw the circuit diagram of repel carry adder. 2+6+4+3
c) Distinguish between SRAM and DRAM. Why do we require memory hierarchy? Show
the memory hierarchy diagram on the basis of speed and cost. Briefly describe the
functionality of associative memory.