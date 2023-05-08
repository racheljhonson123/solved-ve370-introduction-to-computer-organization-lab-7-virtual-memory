Download Link: https://assignmentchef.com/product/solved-ve370-introduction-to-computer-organization-lab-7-virtual-memory
<br>
<h2>Purpose</h2>

In computing, virtual memory is a memory management technique that provides an “idealized abstraction of the storage resources that are actually available on a given machine” which “creates the illusion to users of a very large (main) memory”. [Wikipedia]




In order to support this technique, a virtual address to physical address translation mechanism is created on top of the memory hierarchy we modeled in the last lab, as shown in the following structural diagram.










The virtual to physical translation mechanism typically includes a Page Table and a Translation Look-aside Buffer (TLB), as shown in the following diagram. As discussed in lectures, the relationship between TLB and Page Table resembles that between the cache and main memory.




<strong> </strong>

<h2>Tasks</h2>

<strong> </strong>

Assume the following properties of the memory:

<ul>

 <li>Byte addressable</li>

 <li>Size of virtual address: 14 bits</li>

 <li>Size of physical address: 10 bits</li>

 <li>Size of the main memory: 1024 bytes</li>

 <li>Size of the cache: 64 bytes</li>

 <li>Size of a block: 4 words</li>

 <li>Cache associativity: 2-way associative</li>

 <li>Write technique: write back</li>

 <li>Cache replacement policy: Least Recently Used (LRU)</li>

 <li>Page size: 256 bytes</li>

 <li>Page Table entry size: 4 bytes each</li>

 <li>Size of TLB: 4 ´ 4 bytes</li>

 <li>TLB associativity: fully associative</li>

 <li>TLB Write technique: write back</li>

 <li>TLB replacement policy: LRU</li>

</ul>




When CPU needs to access a data/instruction in the memory, it sends a 14-bit virtual address to the TLB. If there is a hit in TLB, TLB then sends the corresponding physical address to the cache memory. If there is a TLB miss, TLB should then get the physical address from the Page Table, then send the corresponding physical address to the cache memory. If TLB fails to get the physical address from the Page Table, meaning the requested data is not currently in the physical memory, report a page fault.




Model the memory hierarchy and translation mechanism in Verilog HDL. Write a testbench to act like a CPU to provide a sequence of virtual addresses for reading or writing. Pre-load the main memory with randomly generated data by your team. Simulate the functions of the memory hierarchy with a Verilog simulator of your choice.




Notes about the design:

<ol>

 <li>Clock signal is not needed.</li>

 <li>You do not need to implement a FSM.</li>

 <li>You are free to add some new features or new signals, if you think it is necessary.</li>

 <li>For output of main memory, only showing the part whose value has been changed during the simulation process is enough.</li>

 <li>On page fault, just indicate.</li>

 <li>You are free to create your own design, but it should be reasonable, and you need to give a clear explanation to us during demonstration.</li>

 <li>FPGA implementation is not required.</li>

</ol>




<h2>Team Organization</h2>




This lab is a team effort. Each team should consist of 3 students, randomly grouped. The work should be appropriately divided and distributed among all team members. Students are not allowed to switch teams without permission of the instructor.







<h2>Deliverables</h2>

<strong> </strong>

<ul>

 <li><strong>Demonstration –</strong> Every team should demonstrate to the teaching group the following before your lab session ends:

  <ul>

   <li>Simulation results of the top-module of your design showing significant events and changes of your memory</li>

   <li>RTL schematic of your Verilog model generated with Xilinx Vivado software</li>

  </ul></li>

</ul>

Each team member should be prepared for an oral exam on this lab during the demonstration.




<ul>

 <li><strong>Peer Evaluation </strong>– Each team member is required to provide a peer evaluation for the team effort in this lab. The marks of the peer evaluation should be integers ranging between 0 to 10, inclusively, with 10 indicating the biggest contribution. A mark should be given to each team member including yourself according the team member’s contribution based on your observation. A brief description of contribution of each team member should also be provided, as shown in the following table.</li>

</ul>




<table width="588">

 <tbody>

  <tr>

   <td width="162">Name</td>

   <td width="162">Level of contribution (0 ~ 10)</td>

   <td width="264">Description of contribution</td>

  </tr>

  <tr>

   <td width="162">(yourself)</td>

   <td width="162"> </td>

   <td width="264"> </td>

  </tr>

  <tr>

   <td width="162">(your lab partner)</td>

   <td width="162"> </td>

   <td width="264"> </td>

  </tr>

  <tr>

   <td width="162">(your lab partner)</td>

   <td width="162"> </td>

   <td width="264"> </td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<ul>

 <li><strong>Source Files – </strong>All your Verilog source files and any other supporting files.</li>

</ul>




This is a 2-week lab. The full score for this lab is 300 points.