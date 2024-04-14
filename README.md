Advanced Physical Design using Openlane/Sky130

     

Inception of Open source EDA, OpenLANE and Sky130PDK

Introduction to QFN-48 Package,Chip,pads,core,die and IP’s
Arduino is a popular open-source electronics platform based on easy-to-use hardware and software. It consists of a microcontroller (originally Atmel AVR family, now expanded to various architectures including ARM) and a development environment for writing software for the microcontroller. Microcontrollers are designed to be compact and contain all essential components on a single chip, including a CPU (Central Processing Unit), memory (both RAM and ROM), timers, and I/O (Input/Output) ports. Microcontrollers are typically programmed using high-level languages such as C or C++, as well as specialized integrated development environments (IDEs) provided by the microcontroller manufacturers. Program code is typically stored in non-volatile memory (ROM or flash memory) and executed by the microcontroller's CPU.
![WhatsApp Image 2024-03-29 at 6 47 59 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/12e695b2-03cf-4737-b188-c3ba56c78bf6)
The circled picture in the above image describes about the processor and its connectivity.
![WhatsApp Image 2024-03-29 at 6 48 14 PM (1)](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/6d47a0a0-a8bc-412c-bce3-50d8990e7db7)

 
The below picture refers to Package. The pin placements are determined by the Arduino board under the development. The connectivity between the chip and the package are illustrated through the wires which determines the transmission of signals in and out of the chip.
![WhatsApp Image 2024-03-29 at 6 49 08 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/4cd0a379-61f8-498d-a829-72d458ed809c)

 
Components:
![WhatsApp Image 2024-03-29 at 6 49 25 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/42b03df6-3580-4461-98e8-50bc169df078)

 
1.	Pads:
•	Pads refer to the interface between the chip and the outside world. They are the connection points on the integrated circuit (IC) where signals enter and exit the chip. Pads are typically arranged around the periphery of the chip and are used for various purposes such as power supply, ground, input/output (I/O), and test/debugging.
2.	Core:
•	In semiconductor design, the core usually refers to the central processing unit (CPU) or the main computational unit of a chip. It is the part of the chip responsible for executing instructions, performing calculations, and managing data processing tasks. In more general terms, a core can also refer to a fundamental functional block or module within a chip, such as a processing core, memory core, or graphics core.
3.	Die:
•	Die refers to a single semiconductor chip that has been fabricated on a wafer during the semiconductor manufacturing process. A wafer typically contains multiple copies of the same chip design, known as die. After the fabrication process is complete, the wafer is diced into individual die, each containing a fully functional semiconductor chip.
4.	Macros:
•	Macros, short for macrocells or macroblocks, are predefined functional blocks or modules that can be integrated into a larger chip design. These macros are often used to implement commonly used functions such as memory controllers, input/output (I/O) interfaces, or digital signal processing (DSP) blocks. Integrating macros into a chip design can help reduce design time, minimize development costs, and improve overall design efficiency.
5.	Foundry IP's (Intellectual Property):
•	Foundry intellectual property (IP) refers to reusable design blocks or components provided by semiconductor foundries for use in chip designs. Foundry IP's typically include standard cell libraries, memory compilers, I/O libraries, and specialized IP blocks optimized for the foundry's manufacturing process technology. These IP blocks help chip designers accelerate the design process, reduce development risks, and take advantage of the foundry's manufacturing expertise.
In summary, pads provide the interface between the chip and the outside world, the core is the central computational unit of a chip, die refers to individual semiconductor chips on a wafer, macros are predefined functional blocks used in chip designs, and foundry IP's are reusable design components provided by semiconductor foundries to facilitate chip design and manufacturing.


 
Introduction to RISC-V:
RISC-V is an open-source instruction set architecture (ISA) based on Reduced Instruction Set Computing (RISC) principles. In order to execute a C-program on a chip with a particular layout, it has to be compiled into language program like RISC-V. Then this is converted into machine language in a binary format which is easily understood by the computer hardware.
The RISC-V specifications have to be translated to hardware description language(HDL) to pass on layout. So, C Programming is executed and should get automatically executed by the hardware to get the output.
![WhatsApp Image 2024-03-29 at 7 20 22 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/899855cf-e2b3-4a14-b44f-7aabb8e4677f)

 
From Software Applications to Hardware

From a software application to hardware, the concept of macros can be understood in various contexts:

1. *Software Application:* In software applications, macros are often used to automate repetitive tasks or to streamline complex operations. For example, in a spreadsheet program like Microsoft Excel, users can create macros to automate calculations, formatting, or data manipulation tasks. These macros can be recorded by the user performing a series of actions and then replayed to execute the same sequence of actions automatically.

2. *Operating System:* Within an operating system, macros can be used to define system-wide settings or configurations. For instance, in Unix-like systems, shell scripts can include macros to simplify the execution of common tasks or to define environment variables that affect the behavior of various programs.

3. *Programming Languages:* In programming languages, macros are often used to define reusable code snippets or to create domain-specific languages. For example, in the C programming language, macros are defined using the #define directive and can be used to create constants, inline functions, or to implement conditional compilation.

4. *Hardware Description Languages (HDLs):* When it comes to hardware, macros are commonly used in Hardware Description Languages (HDLs) like Verilog or VHDL. In HDLs, macros, often referred to as macros or macros, are used to define reusable hardware components or configurations. These macros can represent complex digital circuits, such as adders, multiplexers, or even entire subsystems. HDL macros are instantiated within larger designs to create hierarchical structures and to facilitate modular design practices.

5. *Electronic Design Automation (EDA) Tools:* In the context of electronic design, macros play a crucial role in EDA tools such as synthesis and place-and-route tools. Macros in this domain represent predefined blocks of hardware that have been optimized for performance, power, or area. These macros can be instantiated multiple times within a design to achieve scalability and efficiency.

Overall, macros bridge the gap between software and hardware by providing a mechanism for abstraction, automation, and reusability in both domains. Whether in software applications, operating systems, programming languages, or hardware design, macros help streamline development processes and improve productivity.
![WhatsApp Image 2024-03-29 at 7 21 28 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/a4758237-bec1-4c02-a4aa-9e34c99ece4b)

 
 Flow: Stopwatch app to Hardware
 ![WhatsApp Image 2024-03-29 at 7 21 42 PM (1)](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/9978f9b9-ee8c-4e50-a5d6-8689cc52fd84)

 
Flow: ISA->HDL->Netlist->Physical design
SoC design and OpenLANE
Introduction to all components of opensource digital asic design:
To design an ASIC, we require RTL designs, EDA tools and PDK data.
![Screenshot 2024-03-25 212234](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/08148502-c7c6-4e11-9a43-9d0905154a71)

 
1.	RTL IP's (Register Transfer Level Intellectual Property):
•	RTL IP refers to pre-designed and pre-verified functional blocks or modules described at the Register Transfer Level (RTL), which is a level of abstraction in digital design representing the flow of data between registers in a digital circuit. RTL IP's are typically used as building blocks in the design of larger integrated circuits (ICs) or Systems-on-Chip (SoCs). Examples of RTL IP's include processor cores, memory controllers, interface controllers (e.g., USB, PCIe), and specialized accelerators (e.g., DSP, cryptography).
2.	EDA Tools (Electronic Design Automation Tools):
•	EDA tools are software applications used by semiconductor and electronic design engineers to design, verify, simulate, and test electronic systems and integrated circuits (ICs). These tools automate various stages of the design process, from logic design and synthesis to physical design, verification, and manufacturing. Common categories of EDA tools include:
•	RTL Design Tools: Used for designing and verifying digital logic at the Register Transfer Level (RTL).
•	Synthesis Tools: Convert RTL descriptions into gate-level netlists optimized for specific target technologies.
•	Simulation Tools: Verify the functional correctness of the design through simulation at various levels of abstraction (RTL, gate-level, transistor-level).
•	Place and Route Tools: Determine the physical layout of components on a chip and the routing of interconnects between them.
•	Timing Analysis Tools: Ensure that the design meets timing constraints and performance requirements.
•	Physical Verification Tools: Check the design for manufacturing-related issues such as design rule violations, layout errors, and electrical rule violations.
3.	PDK (Process Design Kit):
•	A PDK is a collection of files and models provided by a semiconductor foundry that contains information about the manufacturing process technology used to fabricate integrated circuits (ICs). It includes data such as design rules, device models, parameterized cells (PCells), technology files, and simulation models required by electronic design automation (EDA) tools to design and verify ICs. Designers use PDKs to develop chip designs that are compatible with the manufacturing process offered by the foundry. PDKs are essential for ensuring that chip designs meet the fabrication requirements and constraints of the foundry's manufacturing process.
In summary, RTL IP's are pre-designed functional blocks described at the Register Transfer Level, EDA tools are software applications used for electronic design automation, and PDKs are collections of files and models provided by semiconductor foundries that contain information about the manufacturing process technology used to fabricate integrated circuits. These components play crucial roles in the design, verification, and fabrication of electronic systems and ICs.
![Screenshot 2024-03-25 212756](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/f9709476-c612-480f-baab-abbc3a98c562)
![Screenshot 2024-03-25 212835](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/30955bac-2561-4b20-be36-3abf768e8aed)


 

 
Simplified RTL2GDS flow 
![Screenshot 2024-03-25 213035](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/1f9b87fb-4dd2-413c-a63a-f3163ef02a81)

1.Synthesis: In the synthesis stage, the RTL description is translated into a gate-level netlist using synthesis tools. These tools map the RTL code to standard cell libraries provided by the semiconductor foundry. The resulting gate-level netlist represents the circuit in terms of logic gates and their interconnections.
![Screenshot 2024-03-25 213236](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/5fa87cd1-b312-4a25-9d72-2bfc1082428d)

 
2. Floorplanning: Floorplanning involves partitioning the chip area into functional blocks and allocating resources such as memory, logic cells, and I/O pads. The goal is to optimize the physical layout of the chip to minimize signal delays, reduce power consumption, and meet performance targets.
   ![Screenshot 2024-03-25 213316](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/a3edfc75-026f-43ad-b740-5bc9e1ea2aa1)

 
Power planning is a crucial step in the RTL-to-GDS (Register Transfer Level to Graphic Data System) flow, particularly in the physical design stage of integrated circuit (IC) development. Power planning involves the distribution of power and ground signals throughout the chip to ensure reliable operation and efficient power delivery. In the power grid design stage, the chip's floorplan is overlaid with a grid of power and ground rails to distribute power and ground signals uniformly across the chip. Power planning tools determine the optimal placement of power and ground lines to minimize resistance, reduce voltage drop, and mitigate noise.
![Screenshot 2024-03-25 213344](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/8fc42371-f1fe-410d-bd3d-59857caf928a)



 
3.placement: In the placement stage, the synthesized and optimized logic cells are placed within the chip's floorplan. Placement tools determine the physical locations of logic cells to minimize wire lengths, reduce congestion, and satisfy timing constraints. Advanced placement algorithms consider factors such as signal timing, power distribution, and thermal effects.
![Screenshot 2024-03-25 213422](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/e763c112-cfec-4059-8c26-6088d611e132)
![Screenshot 2024-03-25 213516](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/622a255d-3c1d-4178-be4b-f386da800653)


 

 
4.	Clock Tree Synthesis (CTS): Clock tree synthesis involves the generation of a hierarchical clock distribution network to distribute clock signals uniformly across the chip. CTS tools optimize clock routing to minimize skew, ensure clock signal integrity, and meet timing requirements.
   ![Screenshot 2024-03-25 213533](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/cceb60ed-8ab4-4860-8c96-6634d86e3ef3)

   

 
6.	Routing: The routing stage involves the generation of physical metal interconnects (wires) to connect the placed logic cells according to the synthesized netlist. Routing tools handle the complex task of routing signals while considering design rules, signal integrity, and timing constraints. Global routing establishes the overall routing topology, while detailed routing handles the routing of individual metal tracks.
   ![Screenshot 2024-03-25 213621](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/f319af73-b8bc-43fa-a8e4-e1a05862ad4a)


 
1.	6.Sign off: Functional Verification:
•	Functional verification ensures that the design behaves correctly according to its specifications. Simulation-based techniques, such as RTL simulation and gate-level simulation, are used to verify the functionality of the design under various operating conditions and test scenarios. Functional coverage analysis is performed to ensure that all functional aspects of the design have been adequately exercised.
2.	Timing Closure:
•	Timing closure involves ensuring that all timing constraints are met, including setup time, hold time, clock skew, and maximum operating frequency. Static timing analysis (STA) tools are used to analyze the timing paths in the design and identify timing violations. Design optimization techniques, such as logic restructuring, clock tree synthesis, and placement and routing optimizations, may be applied to achieve timing closure.
3.	Power Integrity Analysis:
•	Power integrity analysis ensures that the power distribution network (PDN) meets the design's power delivery requirements and maintains stable power supply voltages. Analysis techniques, such as power grid integrity checks, voltage drop analysis, and electromigration analysis, are performed to identify and mitigate power-related issues. Decoupling capacitors and power gating techniques may be used to improve power integrity.
4.	Physical Verification:
•	Physical verification checks ensure that the design adheres to design rules, manufacturing constraints, and reliability requirements. Design rule checking (DRC) and layout versus schematic (LVS) checks are performed to identify and correct layout errors, such as spacing violations, overlapping geometries, and missing connections. Electrical rule checking (ERC) verifies the electrical integrity of the design, including signal integrity and power distribution.
5.	Design for Manufacturability (DFM):
•	Design for manufacturability (DFM) checks ensure that the design is manufacturable with high yield and reliability. DFM techniques, such as lithography simulation, metal fill insertion, and manufacturing variability analysis, are employed to identify and address potential manufacturing issues, such as lithography hotspots, electromigration, and process variations.
6.	Reliability Analysis:
•	Reliability analysis evaluates the design's long-term reliability under various operating conditions and stresses, such as temperature variations, voltage fluctuations, and aging effects. Techniques, such as electromigration analysis, stress testing, and accelerated life testing, are used to assess the design's reliability and identify potential failure mechanisms.
7.	Documentation and Release:
•	Once all sign-off criteria have been met, the design is documented, and the final design database, including the GDSII layout file, is released for manufacturing. Design documentation typically includes a sign-off report summarizing the results of all verification and analysis activities, as well as any design constraints, assumptions, and recommendations for manufacturing.
8.	Handoff to Manufacturing:
•	The finalized design database is handed off to the semiconductor foundry for manufacturing. The foundry performs additional checks and optimizations to prepare the design for fabrication, including mask data preparation, reticle layout inspection, and tape-out procedures.




Introduction to OpenLANE and strive chipsets
OpenLane is an automated RTL-to-GDSII (Register Transfer Level to Graphic Data System II) flow for designing integrated circuits. It encompasses a range of tools and scripts to automate various steps in the ASIC design process, from synthesis and placement to routing and timing analysis. OpenLane is built upon the OpenROAD framework, which provides an end-to-end design flow for digital ASICs.
The openlane flow based on several components including OpenROAD, Yosys, Magic, Netgen, CVC, SPEF-Extractor, KLayout and a number of custom scripts for design exploration and optimization.
![Screenshot 2024-03-25 214026](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/b579ee53-bd01-45c4-83a3-bb7be9ccb368)
![Screenshot 2024-03-25 214043](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/9397dbc4-0252-4418-917f-4730bf9dc16e)


 
 
The objective of OpenLANE is to produce a clean GDSII (No LVS violations, No DRC violations, and no Timing violations) with no human intervention.
Introduction to OpenLANE detailed ASIC design flow
![Screenshot 2024-03-25 214710](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/f1e7112d-2501-4aa3-8b88-9439755a4e50)

 
1.	Synthesis Exploration step involves generation of reports showing delay vs area
	![Screenshot 2024-03-25 214945](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/6fb4f761-a122-4898-b399-d293cb109ec2)

 
 
2.	Design Exploration step is used to sweep the design configuration and it's useful to find best configuration for any given design.
	![Screenshot 2024-03-25 215009](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/b1dc1097-c446-48a8-a084-f46bf071360c)

	
  
3.	OpenLANE Regression Testing
	![Screenshot 2024-03-25 215112](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/03832245-6653-4b9a-b5ed-089ffa9281b8)
.	

	
 
4	Design for Test (DFT)
![Screenshot 2024-03-25 215221](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/4f6db246-8be5-46e1-a761-d351467e8468)

 
5.	Physical verification (DRC & LVS)
   ![Screenshot 2024-03-25 215221](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/cc90db56-901d-4821-84b5-3b32e4e0c0db)

   
 
6.	Logic Equivalence Check (LEC) checks the logic synchronisation between physical implementation and the netlist.

   ![Screenshot 2024-03-25 215221](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/06318c95-ae23-4cfc-8f65-ed5a7ad354bf)


    

 7.Dealing with Antenna Rules violations
 ![Screenshot 2024-03-25 215221](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/2dbb8b29-51c9-4bd9-9ecf-acc498268f3b)
 ![Screenshot 2024-03-25 215538](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/e94e5237-d923-4442-9c4c-d5070ba47663)
 ![Screenshot 2024-03-25 215538](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/004c891e-b8d5-4281-96fc-51851aa95c11)
 



 
 
  
8.	Static Timing Analysis (STA) ensures that the design meets timing requirements. STA evaluates the timing behavior of a digital circuit without considering dynamic factors such as signal transitions and clock skew. It determines whether the design meets setup and hold time constraints, maximum clock frequency, and other timing requirements. The input to STA includes the synthesized netlist of the design, and timing constraints.
   Getting familiar to open-source EDA tools:
Openlane Directory structure in detail
The openlane working has the folders and the subfolders.
Getting familiar to open-source EDA tools:
Openlane Directory structure in detail
The openlane working has the folders and the subfolders.
![WhatsApp Image 2024-03-30 at 12 35 14 PM (1)](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/ef99a712-f704-4662-92ba-b893efd041b7)


 
•	open-pdks contains scripts that makes the commerical PDK to also be compatible with the open-source EDA tool
•	sky130A pdk variant is made especially compatible for open-source tools. It contains libs.ref and libs.tech libs.ref contains all the process or technology specific files, example sky130_fd_sc_hd : Sky130nm Foundry Standard Cell High Density libs.tech has files specific for the tool (klayout,netgen,magic...)
•	skywater-pdk contains all Skywater 130nm PDKs
Design Preparation Step
OpenLane can be invoked using docker command using the interactive session. ./flow.tcl -interactive runs the openlane in interactive mode. % package require openlane 0.9 retrives all dependencies for running v0.9 of OpenLANE
![WhatsApp Image 2024-03-30 at 12 35 19 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/e2e83155-0600-4a86-aa93-c2f718f13f7d)


 
Openlane has multiple designs and we need to work on picorv32a inside a specific design folder there is a config.tcl which has the default settings on OpenLANE.

The priority order for the Openlane settings are: sky130_xxxxx_config.tcl in OpenLane/designs/[design]/ config.tcl in OpenLane/designs/[design]/ default values in OpenLane/configuration/
![WhatsApp Image 2024-03-30 at 12 35 19 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/28b4a06e-1818-44d7-92d9-eb52da5c3985)

 
Setup the design stage for the flow and to begin with synthesis of a design
prep -design picorv32a
The above command when executed, sets up the filesystem where the OpenLANE tools can dump the outputs. This creates a run/ folder inside the picorv32a directory which contains the command log files, results, and the reports dumped by each tool. The folder will be empty for now except for lef files generated by this design setup stage. The cell LEF files .lef and technology LEF files .tlef merge to generate merged.lef inside run/tmp/
![WhatsApp Image 2024-03-30 at 1 06 06 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/52b30863-c916-43d0-a65c-95f7d97191f5)
![WhatsApp Image 2024-03-30 at 1 08 42 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/e4bc9da4-0042-4d67-8f6d-e7a9b2879a8c)


 
 
Review files after design prep, run synthesis, and characterize synthesis results
Run synthesis with the command: run_synthesis  runs by yosys, RTL synthesis, ABC scripts (for technology mapping) and openSTA.
![WhatsApp Image 2024-03-30 at 1 13 15 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/45d5ab4d-dbc5-443b-9f34-ef59b3ef33b7)

 
Results after synthesis is as follows.
![WhatsApp Image 2024-03-30 at 12 35 28 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/8f645f24-df29-4adf-adfd-703c996d87c1)
![WhatsApp Image 2024-03-30 at 12 35 27 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/b1fac3b4-aba8-4c25-acfd-db1cc63a1089)


 
 
 
Here the DFF count: sky130_fd_sc_hd__dfxtp_2 = 1613
And total number of cells = 14876
D flip-flop ratio = count of DFFs / total number of cells = 1613 / 14876 = 0.108429685 (OR) 10.8429 %
After running synthesis, inside the runs/[date]/results/synthesis is picorv32a_synthesis.v which is the mapping of the netlist to standard cell library using ABC. The runs/[date]/reports/synthesis will contain synthesis statistic reports and STA reports. The log files are:
![WhatsApp Image 2024-03-30 at 1 17 55 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/54748684-07bc-4a12-bc89-2602c249f0c1)

 
Good floorplan vs bad floorplan and introduction to library cells
Chip Floor planning considerations
Utilization factor and aspect ratio
1.	Define width and height of core and die
Core: The core refers to the central functional area of the integrated circuit where the actual circuitry and logic reside. The width and height of the core typically refer to the dimensions of this functional area, which contains the active components of the chip, such as logic gates, memory cells, and other functional blocks. The width and height of the core are essential parameters that influence the overall size and aspect ratio of the chip.
2.	Die: The die represents the individual unit of an integrated circuit that is fabricated on a semiconductor wafer during the manufacturing process. The die contains the entire functional circuitry of the chip, including the core, as well as additional features such as bonding pads, I/O interfaces, and metal layers for interconnections. The width and height of the die correspond to the dimensions of the rectangular or square-shaped semiconductor substrate on which the circuitry is fabricated.
In summary, the width and height of the core and die of an integrated circuit refer to the dimensions of the functional circuit area and the entire semiconductor substrate, respectively. These dimensions are critical parameters in IC design and manufacturing, ifluencing factors such as chip size, layout optimization, and packaging considerations.
![Screenshot 2024-03-27 214319](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/2f79e627-bfc1-4ce0-868f-85d60fc61069)
![Screenshot 2024-03-27 195433](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/9cb49a94-34a0-4024-a1d9-2d029659a9bb)
![Screenshot 2024-03-27 195350](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/eeaba804-d76d-4149-ac84-28532d66d253)



   
 Let's calculate the area occupied by the above netlist on a silicon wafer. Before that the wires are ignored and the flops and combinational logic are combined together to get the total area. So, here, the area will be 4 sq.units.
 ![Screenshot 2024-03-27 195722](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/0b9e255b-c31a-4cd4-95bf-2addfaf34925)
 ![Screenshot 2024-03-27 195710](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/2b76ecc0-a98a-4620-bbce-d7f0f023e272)
 ![Screenshot 2024-03-27 195924](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/106fae15-edd1-4058-a3b7-4cc2281e80cb)
 ![Screenshot 2024-03-27 195932](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/bcc0effd-94af-47cc-ae4a-dcd95a7660c4)

 



 
 
 
 
 
Utilization factor = (4 x 1sq.unit) / (2 unit x 2 unit) = 1
which means the core is completely occupied. In practical scenario, utilization is about 50%
Aspect ratio = Height / Width
In this case, height and width are same, so the aspect ratio is 1 If the aspect ratio is 1 it shows that the chip is square, otherwise it is rectangle.
Example: 
![Screenshot 2024-03-27 200751](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/b3f2d61e-279b-411e-b039-a7f1ba664af6)


 
1.	Utilization factor = (4 sq.units) / (8 sq.units) = 0.5
Aspect ratio = 2 / 4 = 0.5
Concept of pre-placed cells
2.	Define Locations of Preplaced Cells
Preplaced cells (also known as pre-placed instances or pre-placed blocks) are specific circuit elements within an integrated circuit design layout that are manually positioned in advance by the designer. The locations of preplaced cells are predetermined and fixed before the automated placement and routing stages of the design flow.
the locations of preplaced cells are manually determined by the designer to optimize layout, performance, and connectivity within an integrated circuit design. By strategically positioning these cells and aligning them with key design elements, designers can improve overall chip performance and manufacturability.
Consider the following netlist being divided into two sets of blocks with connectivity preserved.
![Screenshot 2024-03-27 200751](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/7bc02ba9-a740-4bda-9d01-35570a1a8e89)
![Screenshot 2024-03-27 221418](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/e561784d-d1c0-4c6a-ae74-f36a182ef0af)
![Screenshot 2024-03-27 221432](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/b49dd2e5-b54f-4396-ba1c-70d70de986e6)




 

 
 
So, if Block1 has to be used by a designer, it can be directly handed over since it is blackboxed. This block can be used across the designs. It means the block can be reused.
![Screenshot 2024-03-27 221650](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/b3b40b9d-77b4-4fd4-bf70-2113e997f9bf)





De-coupling capacitors
3.	Surround pre-placed cells with decoupling capacitors
![Screenshot 2024-03-27 222030](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/9fb85f4b-2732-447a-a3f3-d49a6adf7880)

 
 
Consider the circuit below as a part of a block. Whenever the circuit switches, there is an amount of current demand. For example, if the AND gate switches from logic0 to logic1, the capacitance has to completely charge. The amount of charge will be sent from the supply voltage. And when the logic switches from logic1 to logic0, the capacitance discharges and it's the responsibility of the Vss to take that discharged current.
In reality, when the Vdd supplies voltage to the circuit, there is a drop due to resistance, inductance and capacitance of the wire and supplied volatge is Vdd'.
![Screenshot 2024-03-27 222138](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/6bde5775-0e15-4500-a4ff-f0f51cfe8d1a
![Screenshot 2024-03-27 222415](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/af1b1b50-e419-49a8-a1aa-50b2c09fc981)


 
 
The Vdd' should be within the noise margin range which is from Vih to Voh. If it is present somewhere in the undefined region, then the logic 1 is unstable. This is because of the large physical distance from the main power supply to the circuit.
![Screenshot 2024-03-27 222450](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/65d48f3c-58a2-414a-9944-863164b16d59)

 
 
Solution to such problem is the addition of decoupling capacitors. We can consider decoupling capacitor as a huge capacitor completely filled with charge. the equivalent voltage across the capacitor is same as seen across the main supply voltage. The capacitor decouples the circuit from the main supply.
![Screenshot 2024-03-27 222847](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/cc23a2b7-b508-4c0b-a57a-b7d8ddcc4d70)
![Screenshot 2024-03-27 222830](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/0265e0ab-63be-4875-a513-9a2d2e97db1d)


 
 
  
Power Planning
Consider the circuit as a macro and it demands more current. Say, it's used as a driver as well as load, and the load should receive the same signal quality as the driver.
![Screenshot 2024-03-27 223524](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/9f619bd5-4d78-4a37-bb84-2a04ddbf0058)

 
 
Decoupling capactor is not feasible to be added all over the chip but only on the critical elements.
![Screenshot 2024-03-27 223616](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/07ac6987-6c46-44b4-bc7c-6a85449869eb)

 
In the below picture, 1 means the capacitor is charged to V and 0 means the capacitor is discharged. If the wire bus is connected to an inverter, then it means that all the capacitors charged to V will discharge at the same time. Large number of elements switching to logic0 might cause Ground Bounce due to huge amount of current that needs to be sinked at the same time, and switcing to logic 1 might cause Voltage Droop due to insufficient current from the power source to all elements. Ground bounce and Voltage Droop might cause the voltage to not be within the noise margin range. The solution is to have multiple powersource taps (power mesh) where elements can source current from the nearest Vdd and sink current to the nearest Vss tap.
![Screenshot 2024-03-27 224046](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/ad05644c-df7b-4382-9113-a7b7eebfc5f4)

![Screenshot 2024-03-27 223858](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/9aba5720-373f-4627-8b82-e57b678f0bba)



  
Instead of single power supply as before, there are multiple Vdd and Vss lines. If a logic demands current, it can tap current from the nearest power supply.
![Screenshot 2024-03-27 224855](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/fde88798-75ae-4e35-96c7-038436ee43a4)
![Screenshot 2024-03-27 225125](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/c1212ff4-665b-48cf-b3df-09894a491318)


  



Pin placement and logical cell placement blockage
Let's take below design as an example to be implemented. The connectivity information between the gates is coded usign VHDL or Verilog language and is called as netlist.
![Screenshot 2024-03-29 111628](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/e4331eab-e114-48e9-838d-42b3b3f2ff54)

 
The input and output ports are placed on the left and right spaces between the core and the die. The placements of the ports depends on where the cells are placed. The clock ports are bigger in size than data ports since the clocks are driving the cells continuously. So, we need the least resistance paths for the clocks. Bigger the size, lesser the resistance.
![Screenshot 2024-03-29 111832](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/c56f4ba5-06ae-43a3-8c15-3b711a836412)
!


 
Once pin/port placement is done, Logical Cell Placement Blockage is created to make sure that the APR tool does not place any cell on the pin locations.
![Screenshot 2024-03-29 112411](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/048a4e6f-de57-44ac-8662-03fda69e7741)


 
 
Steps to run floorplan using OpenLANE and view floorplan layout in Magic
1.	Setting configuration variables: Before running floorplan, the configuration variables or switches must be set. These are present in openlane/configuration directory:
   ![WhatsApp Image 2024-03-30 at 1 17 55 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/be5d5715-afc6-48b5-807a-19cddd515d13)

 
 
The README.md consists of all configuration variables for every stage and the tcl files contain the default OpenLANE settings.
2.	Default parameters are set for floorplan stage in floorplan.tcl in OpenLANE
3.	All configurations/switches accepted by the current run are from openlane/designs/[design]/config.tcl
The priority order from highest to lowest is as follows:

•	openlane/designs/[design]/sky130A_sky130_fd_sc_hd_config.tcl
•	openlane/designs/[design]/config.tcl
•	openlane/configuration/floorplan.tcl
![WhatsApp Image 2024-03-30 at 12 35 30 PM (1)](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/f41b065d-30ca-42ec-a69d-37023d29a865)

 

 

In OpenLANE flow, the vertical and horizontal metals are one more than what we specify. If vertical metal is specified as 4, then it'll be 5, same case for horizontal.
4.	Run floorplan on OpenLane: % run_floorplan
5.	Floorplan output files are generated in this folder openlane/designs/picorv32a/runs/date/results/floorplan/picorv32a.floorplan.def which is a design exchange format, containing the die area and positions. The die area in this file is in database units and 1 micron is equivalent to 1000 database units. Area of die = (554570/1000) microns * (565290/1000) microns = 311829.1653 um^2
6.	To view the layout after floorplan, we use magic tool
Command: magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.floorplan.def &
![WhatsApp Image 2024-03-30 at 12 35 37 PM (1)](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/d8158098-a77d-49e6-808e-7c519ec52fb6)

 
 
Press "s" to select whole die then press "v" to center the view
Point the cursor to a cell then press "s" to select it, zoom into it by pressing "z"
The IO pins are placed in a random equidistant mode as seen below based on the configuration (FP_IO_MODE = 1) set in openlane/configuration/floorplan.tcl
![WhatsApp Image 2024-03-30 at 12 35 39 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/b8d10dd5-1efc-4cc9-b982-fd83f327f81f)

 
 
The components in the layout can be identified by using the "what" command in tkcon window after selecting it.
![WhatsApp Image 2024-03-30 at 12 35 38 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/e366f0dd-b9f9-4bb8-8254-e431046d989d)

 
 
Standard cells are not placed but can be viewed at the bottom left corner of the layout 
Library Binding and Placement
Netlist binding and initial place design
1.	Bind netlist with physical cells
Bind the netlist to physical cells with real dimensions. The physical cells come from a library that contains cells which can have different dimensions, various shapes of the cells, and delay information. Bigger cells have lesser resistance while the functionality is the same. This means that the library has many flavors of cells.
2.	Placement:
   ![Screenshot 2024-03-29 130039](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/8f1937a0-bcce-4c9d-bb83-8766dceb4094)

 
 
Placement is done based on connectivity. For example, FF1 is close to Din1 pin and FF2 close to Dout1 pin and combinational cells placed nearer to FF1 and FF2. This is to reduce delay.
![Screenshot 2024-03-29 130610](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/e1c9e7e1-4060-4aed-b071-af235b8fe857)

 
 
Optimize placement using estimated wire-length and capacitance
This is the stage where we estimate wirelength and capacitance (C=EA/d) and insert repeaters based on that. If the wirelength is more, then to maintain signal integrity, we add repeaters to reduce resistance. Repeaters basically reconditions the original signal and transfers.
![Screenshot 2024-03-29 134306](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/74279864-482f-4e5a-9004-466418c70ed7)

 
 
Congestion aware placement using RePlAce
Run placement on OpenLane: % run_placement
This commmand is a wrapper which does global placement (by RePlace tool), Optimization (by Resier tool), and detailed placement (by OpenDP tool).
Placement is done in two stages:
•	Global Placement : no legalization takes place and uses Half Perimeter Wirelength (HPWL) reduction model.
•	Detailed Placement : legalization happens where the standard cells are placed in stadard rows, and there will be no overlaps of the cells.
The objective of placement is to converge the overflow value. If overflow value progressively reduces during the placement,then it implies that the design will converge and placement will be successful.
After running the placement, output is generated in this folder /openlane/designs/picorv32a/runs/date/results/placement/picorv32a.placement.def
Command: magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.placement.def &
![WhatsApp Image 2024-03-30 at 5 57 28 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/6d307b11-287d-4081-b713-6dc8779e7458)

 
 
Cell design and characterization flows
All standards cells (AND, OR, BUFFER, INVERTER, flip-flops etc.) are present in standard cell library. The cells inside the library are of different flavors (different drive strengths, functionality, threshold voltage). If the cell size is more, then the drive strength is high to drive longer wires. If the threshold voltage is high, then it will take more time to switch than the one with lesser threshold voltage.
![Screenshot 2024-03-29 141332](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/826eda1a-52ab-474e-b2b9-8a481c6ae6b8)

 
  
•	DRC & LVS Rules: tech files and poly substrate parameters
•	SPICE Models: Threshold, linear regions, saturation region equations with added foundry parameters, including NMOS and PMOS parameteres
•	User defined Spec: Cell height, cell width (drive strength), supply voltage, pin locations, metal layer requirement
•	The standard cell library developer must adhere to the rules given so that when the cell can be used on a real design without any errors
•	Circuit design is done modeling the pmos and nmos to meet input library requirement
•	Layout design is done using Euler's path and stick diagram on Magic layout too
Steps of characterization flow:
1.	Read the spice model files
2.	Read the extracted spice netlist
3.	Define/Recognise the buffer behavior
4.	Read the subcircuits
5.	Attach the necessary power sources
6.	Apply stimulus
7.	provide necessary output capacitance
8.	provide simulation command
   ![Screenshot 2024-03-29 144016](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/218618fc-059d-4285-b591-85a2d4f28b23)
  	![Screenshot 2024-03-29 144001](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/0c73bdfa-bd73-435a-a066-5a9b11e6dc5b)


  
 
 
Steps 1 to 8 are fed in the form of configuration file to the characterization software called "GUNA".
![Screenshot 2024-03-29 144041](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/dc224f04-b6f0-4436-8989-c32ad1bdab55)

 
 
Timing characterization
Syntax and semantics of power.lib, timing.lib and noise.lib. These are necessary to understand the GUNA software workflow.
We are taking inverters connected back to back as an example.
![Screenshot 2024-03-29 144804](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/5b15ed29-2dd5-439d-bd8e-494057183a3e)

 
 
Timing thershold definitions:
![Screenshot 2024-03-29 144814](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/435459bf-4a4a-4647-bf4c-a050d3280b15)

 
 
Two inverters in series, red is output of first inverter and blue is output of second inverter:
![Screenshot 2024-03-29 145038](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/cdb7de66-0ae9-49d9-94e2-df38b081897c)


 
The red is input waveform and blue is output waveform of the buffer. The left side is rise delay and right side is fall delay.
PROPOGATION DELAY= time(out_*_thr)-time(in_*_)
TRANSITION DELAY=time(slew_high_*_thr)-time(slew_low_*_thr)
Negative propagation delay is not expected. This means that the output comes before the input so it's important to choose correct threshold point to produce positive delay. Delay threshold is usually 50% and slew rate threshold is usually 20%-80%.
![Screenshot 2024-03-29 145159](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/2d6990e5-40b5-4380-8d1c-4a23bc7b7d15)

 
 
Design library cell using Magic Layout and ngspice characterization
Labs for CMOS inverter ngspice simulations
IO placer revision
Configuration settings in OpenLANE can be changed in the shell itself, on the fly. For example, to make IO_mode not to be "random equidistant",
% set ::env(FP_IO_MODE) 2 
The IO pins will not be equidistant in mode 2 (default of 1). On re-running floorplan, we can see that the pins are placed based on of the Hungarian algorithms. The pins are stacked one over the other. However, changing the configuration on the fly will not change the runs/config.tcl, the configuration will only be available on the current session.
![WhatsApp Image 2024-03-30 at 6 16 37 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/31275267-bf23-40f3-9a12-bbb8ce6d72c9)


 
 
To echo current value of variable,
echo $::env(FP_IO_MODE)
SPICE deck creation and simulation for CMOS inverter
SPICE deck comprises of connectivity information about the netlist, inputs to be provided to the simulation, information on tap points at which output will be taken and so on. Component values in SPICE DECK: For PMOS, W/L (0.375u/0.25u means width is 375nm and lengthis 250nm). PMOS should be wider (atleast 2x or 3x) than NMOS. PMOS hole carrier is slower than NMOS electron carrier mobility, so to match the rise and fall time, PMOS must be wider (less resistance thus higher mobility) than NMOS. But in this case, we are taking same sizes for both PMOS and NMOS. The gate voltage is normally a multiple of length (250nm) (in the example, gate voltage can be 2.5V)
SPICE deck:
•	component connectivity
•	component values
•	identify nodes
•	name nodes
![Screenshot 2024-03-29 211450](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/1d089073-3856-4d18-81e5-c81fb07278e7)

 
 
SPICE deck netlist description:
•	Syntax for the PMOS and NMOS: [component name] [drain] [gate] [source] [substrate] [transistor type] W=[width] L=[length]
•	All components are described based on nodes and its values
•	.op is the start of SPICE simulation operation where Vin will be sweep from 0 to 2.5 with 0.05V steps
•	tsmc_025um_model.mod is the model file containing the technological parameters for the 0.25um NMOS and PMOS
![Screenshot 2024-03-29 211916](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/4d25dd95-bf8d-47c1-b6ee-bfbf9d65226c)

 
 
SPICE simulation:
 
The steps to follow for SPICE simulation,
1.	Go to ngspice simulator
2.	Source the .cir spice deck file
3.	Execute the spice file by command: run
4.	Execute command: setplot --> allows you to view any plots possible from the simulations specified in the spice deck
5.	Select the simulation desired by entering the simulation name in the terminal
6.	Execute command: display --> to see which nodes available for plotting
7.	Execute command: plot out vs in We can see the plot for above inputs. In this the width of both PMOS &NMOS is same.
   ![Screenshot 2024-03-29 212121](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/e69cbb03-a413-4c5a-a4fe-aac3f0238aa6)

 
 
 
 
Switching Threshold Vm
![Screenshot 2024-03-29 213110](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/419e528e-830a-4bef-a565-4e1539c5c457)

 
 
1.	The shapes are almost the same which means that CMOS is a robust device.
2.	Parameters that defines the robustness of CMOS
o	switching threshold, Vm. It is the point where the Vin = Vout and both PMOS & NMOS are in saturation region. These will be turned on and there is high chances for leakage. There is a high possibility that the current flows directly from VDD to GND. Due to this, short circuit kind of device is seen.
![Screenshot 2024-03-29 213406](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/b594fcea-68b3-4d07-b39a-d740e1b65b9e)

o	 

 
•	Propagation delay: rise or fall delay
Static and dynamic simulation of CMOS inverter
DC transfer analysis is used for finding switching threshold. Simulation is DC sweep from 0V to 2.5V with 0.05V steps:
When a pulse is applied to the CMOS, transient analysis is used to find propagation delay.
![Screenshot 2024-03-29 213619](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/33e1126d-a5e1-457d-abb3-02045c83f7e0)

 

 
 
Lab steps to gitclone vsdstdcelldesign
Instead of designing an inverter from scratch, a github repository where this is already done is cloned to observe the layout.
1.	Clone custom inverter standard cell design from github repository
2.	Change directory to openlane: cd ~/Desktop/work/tools/openlane_working_dir/openlane
3.	Clone the repository with custom inverter design: git clone https://github.com/nickson-jose/vsdstdcelldesign
4.	Copy tech file to the vsdstdcelldesign directory: cp /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech /home/vsduser/Desktop/work/tools/openlane_working_dir/openlane/vsdstdcelldesign/
5.	Open custom inverter layout in magic: magic -T sky130A.tech sky130_inv.mag &
Snippet of commands executed:
![WhatsApp Image 2024-03-30 at 6 33 42 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/7e4d7dc1-3832-4448-90a1-46087ad0d7b8)

 
 
Snippet of sky130_inv:
![WhatsApp Image 2024-03-30 at 6 34 05 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/6ce5ec9e-b5bb-49f6-b0b9-ecc1f12f6b0f)

 
 
Inception of Layout CMOS fabrication process
CMOS Fabrication Process (16-Mask CMOS Process):
1.	Select a substrate
   ![Screenshot 2024-03-29 220557](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/5b0efacb-b7a9-40f1-8876-7795d2437932)

 
3.	Create active region for transistors
o	Deposit Silicon Dioxide (SiO2) on the substrate
o	Deposit Silicon Nitride (Si3N4). It is a protection layer to prevent SiO2 layer to grow during oxidation
o	Deposit a layer of photoresist
o	Deposit mask-1 layer on top of photoresist. It covers the photoresist layer that must not be etched away (protects the two transistor active regions)
o	UV light is applied to remove unmasked portions
o	Remove mask-1 and photoresist layers
o	Place in furnace to grow the oxide in the other areas
o	Remove the Si3N4 layer using hot phosphoric acid to have only p-substrate and Sio2
![Screenshot 2024-03-29 220840](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/b8f5540c-fcc1-4367-a915-eb6e3a867cb5)


 
5.	N-Well and P-Well formation
o	Deposit photo resist layer to define the areas to protect
o	Deposit mask-2. Mask 2 protects the N-Well (PMOS side) while P-Well (NMOS side) is being fabricated then Mask 3 protects P-Well while N-Well is being formed
o	UV light is applied, and the exposed area of photoresist will be removed
o	Boron is used to form P-Well
o	Phosporus is used to form N-well
o	Place in furnace to diffuse boron and phosphorous to form wells. This process is called Twintub process.
![Screenshot 2024-03-30 104952](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/24be3bfe-98c0-48ea-8dd1-68063659034c)

 
7.	Formation of gate terminal
Gate terminal is where the threshold voltage is controlled.
![Screenshot 2024-03-30 104607](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/ef492bb5-7399-4899-bb25-00f8411fe5ac)

 
 
o	Deposit photo resist layer to define the areas to protect
o	Deposit mask-4
o	UV light is applied, and the exposed area of photoresist will be removed
o	Implant low energy boron at the surface of p-well using mask-4 to control the threshold
o	Implant phosphorous/arsenic for n-well using mask-5
o	Fix the oxide which is damaged by implantation steps by removing extra SiO2 using the hydroflouric acid and re-grow high quality SiO2 on p-substrate to contol the oxide thickness
o	Add polysilicon film
o	Add mask-6 and etch using photolithography
o	Etch off to form the gate terminal

 
5.	Lightly Doped Drain (LDD) formation
Two reasons for LDD: hot electron effect & short channel effect
o	Mask 7 for NMOS (lightly doped N-type)
o	Mask 8 for PMOS (lightly doped P-type)
o	Heavily doped impurity (N+ for NMOS and P+ for PMOS) is for the actual source and drain but the lightly doped impurity will help maintain spacing between the source and drain and prevent hot electron effect and short channel effect.
o	To protect the lightly doped regions, add SiO2 and create spacers using plasma anisotropic etching
 
6.	Source and Drain formation
o	Thin screen oxide is formed to avoid channeling. Channeling is when implantations dig too deep into substrate.
o	Mask-9 is for N+ implantation and Mask-10 for P+ implantation
o	The side wall spacers maintain the N-/P- while implanting the N+/P+
o	High temperature annealing is done
 
7.	Local interconnect formation
o	Contacts and interconnects are important to control the electrical characteristics by the designer.
o	Remove thin screen oxide to open up the source, drain and gate for building the contacts.
o	Titanium has less resistance and hence used
o	TiSi2 is used for local interconnects
o	Mask 11 is formed and TiN is etched off using RCA cleaning to create first level contact
 
8.	Higher level metal formation
o	CMP (Chemical Mechanical Polishing) technique to planarize the surface
o	Create contact holes using photolithograhy process
o	Mask 12 is for first contact hole
o	Mask 13 is for first Aluminum contact layer
o	Mask 14 is for second contact hole
o	Mask 15 is for second Aluminum contact layer
o	Mask 16 is for making contact to topmost layer
![Screenshot 2024-03-30 110731](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/9726ed40-0779-4f30-ad56-67eadd014015)

 
 
Lab introduction to Sky130 basic layers layout and LEF using inverter
![WhatsApp Image 2024-03-30 at 6 42 37 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/c11ea7aa-3722-4bdf-9b78-66d79d258e14)

 
 
In sky130A, the first layer is local-interconnect layer or local-i and then the m1, m2 and so on. Power and Ground lines are in m1. When polysilicon crosses ndiffusion the it is NMOS and if polysilicon crosses pdiffusion then it is PMOS is created. The output of the layout is the LEF file. It is used by the router in APR to get the location of standard cell pins to route them properly. So it is basically the abstract form of layout of a standard cell.
Commands in tkcon window for spice extraction of the custom inverter layout:
1.	extract all
2.	ext2spice cthresh 0 rthresh 0 --> this extracts the parasitic information
3.	ext2spice

 
Sky130 Tech File Labs
1.	Lab steps to create final SPICE deck using Sky130 tech
The default SPICE deck file using Sky130 is as seen in the previous section. Now we modify the file to plot a transient response. The final SPICE deck file is as below.
 
Command to load spice file for simulation in ngspice:
ngspice sky130A_inv.spice
Generate a graph using:
plot y vs time a
 
2.	Lab steps to characterize inverter using sky130 model files
   ![WhatsApp Image 2024-03-30 at 6 46 50 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/565b7d53-a320-4f6b-8def-ca0da4e5c1fc)

  
Using the above transient plot, we will now characterize the slew rate and propagation delay:
Maximum voltage = 3.3V 80% of maximum voltage = 2.64V 20% of maximum voltage = 0.64V 50% of maximum voltage = 1.65V
o	Rise Transition (output transition time from 20% to 80%):
	Tr_r = 2.20278ns - 2.15946ns = 0.04332ns
 
o	Fall Transition (output transition time from 80% to 20%):
	Tr_f = 4.06818ns - 4.04073ns = 0.02745ns
 
o	Rise Delay (delay between 50% of input and 50% of output) that is time taken for output to rise to 50% and time taken for input to fall to 50%:
	D_r = 2.18381ns - 2.15003ns = 0.03378ns
 
o	Fall Delay (delay between 50% of input and 50% of output) that is time taken for output to fall to 50% and time taken for input to rise to 50%:
	D_f = 4.05402ns - 4.0501ns = 0.00392ns
 
Magic Tutorial
3.	Lab introduction to Sky130 pdk's and steps to download labs
Commands to download and view the corrupted skywater process magic tech file and other files to perform drc corrections:
o	Command to download the lab files: wget http://opencircuitdesign.com/open_pdks/archive/drc_tests.tgz
o	Extract it: tar xfz drc_tests.tgz
o	Change directory into the lab folder: cd drc/drc_tests
o	List all files: ls -al
o	Command to open magic tool: magic -d XR
4.	Lab introduction to Magic and steps to load Sky130 tech-rules
Useful websites:
Magic Technology File Format Manual - This site explains about tech files. All technology specific information comes from a technology file. This file includes information as layer types, electrical connectivity, design rules, rules for mask generation, rules for extracting netlists etc.
Rules for SkyWater SKY130 PDK
Steps:
o	Open magic with met3.mag as input
![WhatsApp Image 2024-03-30 at 6 51 17 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/c6789e40-d7b4-47f2-a677-e9355a74c9d0)

 
 
o	In this view, we see a number of independent layouts containing some DRC errors
![WhatsApp Image 2024-03-30 at 6 51 38 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/664cda88-9d46-4a1f-8c78-62e3b4cc874c)

 
 
5.	Lab exercise to fix poly.9 error in Sky130 tech-file
o	In tkcon window: load poly
![WhatsApp Image 2024-03-30 at 6 52 08 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/c6b14def-d4d0-4498-8cea-8acb8e622224)

 
 
o	Let's look at rule poly.9 As described in Rules for SkyWater SKY130 PDK, Poly resistor spacing to poly or spacing (no overlap) to diff/tap should be atleast 0.48um.
![WhatsApp Image 2024-03-30 at 6 52 29 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/1f9ac795-3872-425d-85f4-a724a36b7fe1)

 
 
That's not the case here, so we have to fix the tech file to include this DRC.
o	Open sky130A.tech file in drc_tests directory. The included rules for poly.9 are only for the spacing between the n-poly resistor with n-diffusion and the spacing between the p-poly resistor with diffusion. We will now add new rules for the spacing between the poly resistor with poly non-resistor. Highlighted in green below are the two newly added rules. First one is the rule for the spacing between the p-poly resistor with poly non-resistor and the next one is the rule for spacing between n-poly resistor with poly non-resistor. The allpolynonres is a macro under alias section of techfile.
![WhatsApp Image 2024-03-30 at 6 53 06 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/28fed039-870c-4b4d-8f7a-795334a990c1)
![WhatsApp Image 2024-03-30 at 6 53 36 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/156ba88f-fb5f-4933-89e6-90763b56c8f3)


 
  
 
o	In tkcon window: tech load sky130A.tech to check drc in tkcon window: drc check
The new DRC rules will now take effect.
![WhatsApp Image 2024-03-30 at 6 53 57 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/f3bf9e3f-c4fc-4b26-b01b-8e5e011e9a8b)

 
 
6.	Lab exercise to implement poly resistor spacing to diff and tap
To fix what is hown in below pic, modify the tech file to include not only the spacing between npolyres with N-substrate diffusion in poly.9 but also between npolyres and all types of diffusion.
![WhatsApp Image 2024-03-30 at 6 54 20 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/fdea4fd7-bfb8-4f6e-af74-e06f0a5b0a30)

 
 
Pre-layout timing analysis and importance of good clock tree
Timing modelling using delay tables
Lab steps to convert grid info to track info
sky130_inv.mag contains all information like PG information, port information, logic etc. OpenLANE is a PnR tool and a PnR tool does not require all the information present in .mag file. The only information that we'll be needing is the boundary, power and ground rails, and the inputs & outputs. This is the reason of using .lef files. So the objective is to extract the LEF file from Magic file and plug into picorv32a design.
From PnR point of view, there are few guidelines to be followed while making standard cell,
•	The input and output ports lies at the intersection of the horizontal and vertical tracks (ensure the routes can reach that ports).
•	The width of the standard cell must be odd multiple of the tracks horizontal pitch and height must be odd multiples of tracks vertical pitch
Tracks refer to the horizontal and vertical metal layers on which routing occurs. The grid formed by the intersection of horizontal and vertical tracks creates a routing grid, also known as a routing matrix. The ~/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/openlane/sky130_fd_sc_hd/tracks.info contains track information.
Before changing grid:
![WhatsApp Image 2024-03-30 at 6 54 50 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/1265c25d-4d5d-4bdf-b2a3-7c25b781122d)


 
 
After changing grid values:
![WhatsApp Image 2024-03-30 at 6 55 13 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/34c5174b-a1e9-45ee-8072-a66db8c5d3bc)
![WhatsApp Image 2024-03-30 at 6 55 36 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/82bcc10b-c43b-4f48-8f96-574613175261)


 
 

This satisfies the first guideline mentioned above.
![WhatsApp Image 2024-03-30 at 6 55 59 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/bf82530f-edfd-451e-8032-6c8587977830)

 
 
Second requirement is satisfied in below picture.
![WhatsApp Image 2024-03-30 at 6 56 24 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/4cd0ef31-1c66-44a9-be27-2cb650391e51)

 
 

Lab steps to convert magic layout to std cell LEF
LEF (Library Exchange Format) file is a standard file format used to describe the physical layout and characteristics of standard cell libraries or macro libraries. LEF files contain detailed information about the geometric shapes, sizes, layers, and other physical properties of individual cells or macros within the library. The instructions to set the port definitions are in this site
Next, save the .mag file with a new filename. In the tcon terminal: lef write 
It will generate a LEF file with the new filename.
 
Introduction to timing libs and steps to include new cell in synthesis
Inside pdks/sky130A/libs.ref/sky130_fd_sc_hd/lib/ are the liberty timing files for SKY130 PDK which contains the timing and power parameters for each cell needed in STA. It can either be slow, typical, fast with different supply voltages (1v80, 1v65, 1v95). These are called PVT corners. The library name sky130_fd_sc_hd__ss_025C_1v80 describes the PVT corner as slow-slow (delay is maximum), 25° Celsius temperature, at 1.8V power supply. Timing and power parameter of a cell is obtained by simulating the cell in a variety of operating conditions (different corners) and these data are represented in the liberty file. The liberty file characterizes all cells and is used during ABC mapping during synthesis stage which maps the generic cells to the actual standard cells available in the liberty file.
1.	Copy the extracted lef file sky130_vsdinv.lef and the liberty files sky130*.lib from /openlane/vsdstdcelldesign/libs to the src directory of picorv32a. 
2.	Add the folowing to config.tcl inside the picorv32a:
   ![WhatsApp Image 2024-03-30 at 6 56 50 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/3214ecc6-6af9-4295-a743-6f47e0f25a2c)

 
This sets the liberty file that will be used for ABC mapping of synthesis (LIB_SYNTH) and for STA (_FASTEST,_SLOWEST,_TYPICAL) and also the extra LEF files (EXTRA_LEFS) for the customized inverter cell.
3.	Run docker and prepare the design picorv32a. Plug the new lef file to the OpenLANE flow.
docker
./flow.tcl -interactive
package require openlane 0.9
prep -design picorv32a
set lefs [glob $::env(DESIGN_DIR)/src/*.lef]
add_lefs -src $lefs
4.	Next run_synthesis. sky130_vsdinv cell is successfully included in the design
![WhatsApp Image 2024-03-30 at 6 57 14 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/3d545e06-2e6f-4b7c-a24e-0961ed023c15)

 
 
5.	However timing is not met, so it has to be fixed.
   ![WhatsApp Image 2024-03-30 at 6 57 34 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/4f63322b-0bb7-491b-9473-adb971a05dea)

 
 
Delay tables
Whenever the enable pin is 1, only then the CLK will propogate to Y in case of AND gate and whenever the enable pin is 0, only then the CLK will propogate to Y in case of OR gate, as shown below. When the enable is 1, the CLK will not propagate and there won't be any short circuit power consumption and switching power consumption when such elements are used in clock tree. This method is referred to as the clock gating technique.
Consider the below clock tree structure.
![Screenshot 2024-03-30 112453](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/1c3725ce-174e-4a06-9474-bcc5d2f23a2e)

 
 
Buffers on different levels have different capacitive loads and buffer sizes but as long as they have the same loads and sizes in the same level, the total delay for each clock tree path will be the same thus skew will remain zero. Practically, different levels can have varying input transition and output capacitive load and hence varying delay.
Delay tables are used to capture the timing model of each cell and is included inside the liberty file. The main factor in delay is the output slew. The output slew depends on capacitive load and input slew. The input slew is a function of previous stage buffer's output capacitive load and input slew and has its own transition delay table.
![Screenshot 2024-03-30 113149](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/cf128305-42c3-4af8-abc3-d5715be57368)

 
 
At level 2, both the buffers have identical delays with same transition times, load capacitances, and buffer sizes. Consequently, the skew is maintained at 0.If this is not the case, then the skew will be negative leading to timing violations. While these considerations may seem insignificant when analyzing the delay of just two buffers, their significance is high in designs featuring millions of cells. Failing to adhere to these guidelines during clock tree creation can lead to numerous timing-related complications.
Terminologies:
•	CTS is the process of designing a clock distribution network to minimize skew and ensure synchronous operation of the circuit
•	Skew refers to the variation in clock signal arrival times
•	Latency is the delay experienced by the clock signal
•	Slew rate is the rate of change of the signal's voltage over time
Lab steps to configure synthesis settings to fix slack
Currently, tns = -711.59 wns = -23.89 Chip area for module picorv32a = 147712.9184
Next step is to see if synthesis can be more timing-driven.
1.	Check synthesis strategy and other timing related variables and modify accordingly
SYNTH_STRATEGY of delay 0 means the tool will focus more on optimizing the delay, index can be 0, 1, 2, or 3 where 3 is the most optimized for timing at the cost of area. SYNTH_BUFFERING of 1 ensures buffer will be used on high fanout cells to reduce wire delay. SYNTH_SIZING of 1 will enable cell sizing where cell will be upsized or downsized as needed to meet timing. SYNTH_DRIVING_CELL is the cell used to drive the input ports and is vital for cells with a lot of fan-outs since it needs higher drive strength.
 
2.	Run synthesis again and it is seen that area is increased but there is no negative slack
tns = 0 wns = 0 Chip area for module picorv32a = 209181.872
 
 
3.	Run floorplan and placement
If any error comes related to macro placement, temporary solution is to comment basic_macro_placement inside the OpenLane/scripts/tcl_commands/floorplan.tcl (this is okay since we are not adding any macro to the design).
(or)
init_floorplan
place_io
global_placement_or
detailed_placement
tap_decap_or
detailed_placement
After successful run, runs/[date]/results/placement/picorv32a.placement.def will be created.
![WhatsApp Image 2024-03-30 at 7 18 45 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/710ff79c-9629-46c2-8f28-fc82affed68a)

 
 
Search for instance of cell sky130_vsdinv inside the DEF file after placement stage: cat picorv32a.placement.def | grep sky130_vsdinv
Select a single sky130_vsdinv cell instance from the list dumped by grep (e.g. 41096). On tkcon, command % select cell 41096 then ctrl+z to zoom into that cell. As shown below, our customized inverter cell sky130_myinverter is sucessfully placed. Use expand on tkon to show the footprint of the cell and notice how the power and ground of sky130_vsdinv overlaps the power and ground pins of its adjacent cells.
![WhatsApp Image 2024-03-30 at 7 21 40 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/1bca0486-5029-4911-a057-9e6cc80751d5)
![WhatsApp Image 2024-03-30 at 7 22 05 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/5b1e3f5c-1d92-4f09-aa9d-e8151320db6f)
![WhatsApp Image 2024-03-30 at 7 22 19 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/b721a562-b4f8-49f7-a552-84b41b346e5d)



 
 
 

Timing analysis with ideal clocks using openSTA
Setup timing analysis and introduction to flip-flop setup time
Consider an ideal clock where clock tree is not built and perform timing analysis to understand the parameters. Later the same can be done using real clocks. Specifications are as mentioned in the picture. Clock frequncy (F) is 1GHz and clock period (T) is 1ns.
![WhatsApp Image 2024-03-30 at 7 25 45 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/2401ba6b-e5ac-473b-a95c-4b7a1db3ba90)
![WhatsApp Image 2024-03-30 at 7 26 04 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/b1804389-aea1-4945-b662-3a9e76cd6ab8)


 
 

 
Setup timing analysis equation is:
Θ < T - S
Θ = Combinational delay which includes clk to Q delay of launch flop and internal propagation delay of all gates between launch and capture flop
T = Time period, also called the required time
S = Setup time. As demonstrated below, signal must settle on the middle (input of Mux 2) before clock tansists to 1 so the delay due to Mux 1 must be considered, this delay is the setup time.

 
Introduction to clock jitter and uncertainty
Clock is beign created by PLL (Phase Locked Loop). So, this clock source is expected to send clock signal at 0, T, 2T etc. Even these clock sources might or might not be able to provide a clock exactly at Tns because of its own in-built variation. That is called as the jitter. Jitter can be manifested as short-term fluctuations in the timing of signal transitions, resulting in deviations from the expected clock or data timing.
![WhatsApp Image 2024-03-30 at 7 29 22 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/b6c8af31-75f6-485b-aef0-4f78ad37b257)
![WhatsApp Image 2024-03-30 at 7 29 37 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/1cf37161-28a1-4369-b33b-492059a56488)


 
 
 
 
So, a more realistic equation for setup time is,
Θ < T - S - SU
SU = Setup uncertainty due to jitter which is temporary variation of clock period. This is due to non-idealities of PLL/clock source.
![WhatsApp Image 2024-03-30 at 7 29 56 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/49bf8a81-4d50-492f-aa01-cc68dd4684f1)

 
 
Lab steps to configure OpenSTA for post-synth timing analysis
STA can either be single corner which only uses the LIB_TYPICAL library which is the one used in pre-layout(pos-synthesis) STA or multicorner which uses LIB_SLOWEST(setup analysis, high temp low voltage),LIB_FASTEST(hold analysis, low temp high voltage), and LIB_TYPICAL libraries.

 
create_clock command creates clock for the port with specified time period.
set_input_delay and set_output_delaydefines the arrival/exit time of an input/output signal relative to the input clock. This is the delay of the signal coming from an external block and internal delay of the signal to be propagated to external ports. This adds a delay of Xns relative to clk to all signals going to input ports, and delay of Yns relative to clk to all signals going to output ports.
set_max_fanout specifies maximum fanout count for all output ports in the design.
set_driving_cell models an external driver at the input port of the current design.
set_load sets a capacitive load to all output ports.
3.	Execute sta pre_sta.conf and check timing.
Lab steps to optimize synthesis to reduce setup violations
To reduce negative slack, focus on large delays. Net with big fanout might cause delay increase. Use report_net -connections <net_name> to display connections. First thing we can do is to go back to OpenLane and reduce fanouts by setting ::env(SYNTH_MAX_FANOUT) 4 then run_synthesis again.
To further reduce the negative slack, we can also try upsizing the cell with high fanout so that bigger driver will be used. High fanout results in high load cap which then results in high delay. Since we cannot change the load capacitance, we can change the cell size to drive large cap load for less delay.
This can be done iteratively until the desired slack is reached, and this is called Timing ECO (Engineering Change Order).
Clock Tree Synthesis TritonCTS and signal integrity
Clock tree routing and buffering using H-Tree algorithm
Consider the clock port that goes to the flip-flops highlighted in the picture. The purpose is to connect the port to the clock pins of the flip-flops based on the connectivity information. If we blindly connect as shown in the picture below, then t2>t1 and the difference t2-t1 is nothing but the skew. Clock skew refers to the variation in arrival times of the clock signal at different points within a synchronous digital system. In simpler terms, it is the difference in propagation delay experienced by the clock signal as it travels along different paths within the system. Clock skew can occur due to various factors such as differences in wire lengths, variations in signal routing paths, variations in buffer delays, and other physical and environmental factors. These variations can lead to some parts of the system receiving the clock signal earlier or later than others. Minimizing clock skew is essential to ensure proper synchronization of signals and reliable operation of the digital circuit. Ideally, the skew should be zero.
![WhatsApp Image 2024-03-30 at 7 34 03 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/d8dd00c6-b225-495c-a014-ab069e2a71a7)
![WhatsApp Image 2024-03-30 at 7 34 34 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/e9aecd60-391e-491f-befb-87493772ae5b)


  
 
 
 
In the above scenario, the skew is not less/zero, so it is a bad tree.
H-Tree is the solution. It analyses the clock route by calculating the distance from the source to all the endpoints and deciding on a midpoint to start building tree from that point. In this case, the clock reaches at all the endpoints at almost the same time.
![Screenshot 2024-03-30 113826](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/9d4e5b24-5c51-4ead-89ff-1fecde70c2d5)

 
 
We expect that whatever input is provided, that should be reproduced at the output. However, due to the inherent resistance and capacitance in physical wires, the signal may experience attenuation or distortion, hindering its proper transmission to the output. To address this, repeaters or buffers are inserted along the path to ensure signal integrity and reliable transmission.
 
The key difference between repeaters used in clock paths and those used in data paths lies in their rise and fall times. Clock buffers have same rise and fall times, ensuring uniform signal propagation throughout the clock distribution network. In contrast, data buffers exhibit varying rise and fall times, which may differ based on the characteristics of the data being transmitted and the components involved in processing it.

Crosstalk and clock net shielding
Clock nets are critical nets in the design because clock tree is built is such a fashion that the skew is zero. There is a phenomenon called crosstalk where a signal transmitted on one channel unintentionally interacts with or interferes with signals on adjacent channels leading to distortion, noise, timing errors etc. If this happens on clock routes, then the clock tree structure will be deteriorated. So all the clock nets are shielded. By shielding, the clock nets are protected. If there is a wire adjacent to such shields, then there exists a huge coupling capacitance cauign two issues. One is glitch and the other is delta delay.
Whenever there is a switching activity happening on the aggressor, the coupling capacitance is so strong that it directly affects the net sitting close to it called the victim net. the victim net is without any shielding. As a result, there is a dip in the voltage, resulting in glitch.
![WhatsApp Image 2024-03-30 at 7 40 36 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/b726e5ff-d9fc-454f-8b83-2db9d9038c71)

 
 
Shielding basically protects the victim nets by breaking the coupling capacitance between the aggressor and the victim. These shielding nets are either Vdd or Vss. The shields do not switch, so the victim will not switch.
![WhatsApp Image 2024-03-30 at 7 40 57 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/8db38b20-a574-442c-9f4c-07ec57bfe72b)

 
 
Lab steps to run and verify CTS using TritonCTS
After ECO of cell sizing, currently the timing is as follows.
 
The slack might increase or decrease as we move forward in the PnR flow. For OpenLANE to use the current netlist,
 
write_verilog filename overwrites the current verilog file in the specified location.
Then,
run_floorplan
run_placement
Then run cts using the command run_cts. Before that we need to check the default setting s that CTS uses.
 
In CTS stage, clock buffers get added.
 
OpenLANE takes the procs from ~/Desktop/work/tools/openlane_working_dir/openlane/scripts/tcl_commands. These procedures will then call OpenROAD to run the actual tool.
 
For example, run_cts can be found in the file /OpenLane/scripts/tcl_commands/cts.tcl, this tcl procedure will call OpenROAD and will call /OpenLane/scripts/openroad/cts.tcl which contains the OpenROAD commands to run TritonCTS.
Inside the /OpenLane/scripts/openroad/cts.tcl contains the configuration variables for CTS such as:
CTS_CLK_BUFFER_LIST = list of clock buffers used in clock tree branches (sky130_fd_sc_hd__clkbuf_1 sky130_fd_sc_hd__clkbuf_2 sky130_fd_sc_hd__clkbuf_4 sky130_fd_sc_hd__clkbuf_8)
CTS_ROOT_BUFFER = clock buffer used for the root of the clock tree and is the biggest clock buffer to drive the clock tree of the whole chip (sky130_fd_sc_hd__clkbuf_16)
CTS_MAX_CAP = maximum capacitance of the output port of the root clock buffer
Timing analysis with real clocks using openSTA
Setup timing analysis using real clocks
Now the clock tree is built and timing analysis is done on real clocks.
![WhatsApp Image 2024-03-30 at 7 42 10 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/441432dd-a427-41f1-9966-7953ba3c1eca)

 
 
delta1 = launch flop clock network delay delta2 = capture flop clock delay
delta2=capture flop clock delay
 
 
Any design satisfying Slack = Data required time - Data arrival time is ready to work in the given frequency. If this equation is violated , then slack will become negative. We expect slack to be 0 or positive.
Hold timing analysis using real clocks
Hold analysis refers to the delay/time required by the MUX2 model within the flip-flop to transfer data outside. It denotes the duration during which the launch flop must retain data before it reaches the capture flop. Unlike setup analysis, which spans two rising clock edges, hold analysis occurs on the same rising clock edge for both the launch and capture flops. A hold violation occurs when the path is too fast, impacted by factors including combinational delay, clock buffer delays, and hold time. Notably, parameters such as time period and setup uncertainty hold no significance, as both launch and capture flops receive identical rising clock edges during hold analysis.
![WhatsApp Image 2024-03-30 at 7 42 10 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/a438c245-7a78-4c3e-9d8d-f6218f0b0039)
![WhatsApp Image 2024-03-30 at 7 42 39 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/fff80f1d-2a5c-4b18-a75e-3bf7830faa0a)



 
 
Skew = Launch Clock Network Delay - Capture Clock Network Delay

 
 
 
Lab steps to analyze timing with real clocks using OpenSTA
The objective is to analyse the clock tree. Entering into openroad instead of invoking a separate OpenSTA tool. In openroad, timing analysis is done in a different way, where a db is created from lef & def and used.
1.	To create the db, read lef
   ![WhatsApp Image 2024-03-30 at 7 49 44 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/9b4ee8e4-e964-4d38-93f4-bbbd05ce3d45)

 
 
3.	Read def from cts stage
   ![WhatsApp Image 2024-03-30 at 7 50 06 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/5457c7b9-ba9d-4220-8a47-aac66ec89e13)

 
 
5.	Create db
   ![WhatsApp Image 2024-03-30 at 7 50 23 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/726c6950-5ae3-43c7-9fb5-eb70a52ddc29)

   
 
7.	Read the db, verilog file, libraries, sdc
   ![WhatsApp Image 2024-03-30 at 7 51 10 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/044862b4-f8de-4831-a887-bbb6b0d0e170)

 
 

9.	Set propagated clock, it will calculate the actual delay in the clock path.
10.	Check timing
    ![WhatsApp Image 2024-03-30 at 7 51 31 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/df8ad56b-76bf-45ff-941f-515db82fbd6a)
   	![WhatsApp Image 2024-03-30 at 7 51 45 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/803aac9c-0b4a-47cb-83cf-9ffb9249390b)


   
Lab steps to execute OpenSTA with right timing libraries
TritonCTS is built to optimise based on one corner but the libraries that are included in the previous section for timing analysis are min and max corners. This kind of analysis is not accurate. So, exit and re-enter openroad and check timing only for typical corner.
![WhatsApp Image 2024-03-30 at 7 52 00 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/6e17a5fa-0b54-4097-99cb-c45e3d9d1a64)

 
 
 
In this typical scenario, slack is met in both setup and hold analysis.
![WhatsApp Image 2024-03-30 at 7 52 17 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/eb121acb-f657-4c5c-857d-c55f93f028ad)
![WhatsApp Image 2024-03-30 at 7 52 32 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/8b6d4d1f-323a-4a9c-8543-0206238fa18b)


 
 
 
 
When CTS is built, skew values is tried to be met by inserting buffers from the CTS_CLK_BUFFER_LIST. We can also modify this list based on requirements.
When TritonCTS is building the clock tree, it tries to use each buffer listed in $::env(CTS_CLK_BUFFER_LIST) (sky130_fd_sc_hd__clkbuf_1 sky130_fd_sc_hd__clkbuf_2 sky130_fd_sc_hd__clkbuf_4 sky130_fd_sc_hd__clkbuf_8) from smallest to largest until the target skew is met. Target skew is stored in $::env(CTS_TARGET_SKEW). The STA result shows that sky130_fd_sc_hd__clkbuf_1 is the mostly used buffer, we can also change the $::env(CTS_CLK_BUFFER_LIST) to use other buffers and observe the effect on STA and area.
Use tcl lreplace command to modify $::env(CTS_CLK_BUFFER_LIST)
 
The $::env(CURRENT_DEF) used by CTS is the DEF file of the previously run CTS, but the DEF file we want for CTS is the placement's DEF file. So change the $::env(CURRENT_DEF) to point to placement DEF file then run_cts.
Observe the resulting post-CTS STA compared to previous run since we modified the clock buffer. Only buf_2 clock buffer is used now compared to buf_1 used in previous run. The WNS is better now since we used bigger clock buffers.
Final steps for RTL2GDS using tritonRoute and openSTA
Routing and design rule check (DRC)
Introduction to Maze Routing
Routing is to find the best possible connection/route between two points. There are many routing algorithms like Steiner Tree algorithm, Line Search algorithm etc. and one such is Maze Routing - Lee's Algorithm (Lee 1961)
Consider and example of connecting two points 1 & 2. Point 1 will act as a source and 2 will act as a target. The requirement is to find the best possible path or the shortest possible path to connect 1 & 2 will less or no zig-zag routes. Mostly the routes are L-shaped. From algorithmic point of view, the software has to search and connect the two points. From physical designer point of view, it is a physical path/wire establishment for signals to travel between components.

 
Lee's maze routing algorithm, is a popular pathfinding algorithm used in maze routing, which is a type of routing problem where the goal is to find a path from a source to a destination in a maze-like grid. The Lee algorithm is particularly well-suited for routing on grids or mesh-based structures in integrated circuit design.
Algorithm steps:
1.	Initialization: The algorithm starts by initializing a routing grid or matrix representing the maze. Each cell in the grid can be one of several states: obstacle, empty, source, destination, or visited. The source cell is marked with a value of 0, indicating that it is the starting point.
   ![Screenshot 2024-03-30 113624](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/b48cd80e-3078-44b6-afc5-f755febf34c5)

 
 
2.	Wave Expansion: The algorithm performs a wave expansion from the source cell, spreading outwards in all directions. At each step, the algorithm examines neighboring cells (up, down, left, and right) and assigns them a value one greater than the minimum value of their neighboring cells (excluding obstacles). This process continues until the destination cell is reached or until no more cells can be visited.
   ![Screenshot 2024-03-30 113732](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/7da6c5f3-8f52-42fe-bc75-858b448642f9)

 
 
3.	Backtracking and Path Reconstruction: Once the destination cell is reached, the algorithm traces back the path from the destination to the source by following the values in each cell. This results in the shortest path from the source to the destination. There might be multiple paths but the best path that the tool will choose is one with less bends. The route should not be diagonal and must not overlap any blockage/obstruction such as macros or HIPs.
   ![Screenshot 2024-03-30 113759](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/b81c4aea-0007-47b9-9200-5a54fc963761)

   
 
 
 
Design Rule Check
When routing, it's not merely about connecting two points; we must also adhere to specific rules. These rules, for example, mention that when constructing two wires, there must be a minimum spacing or distance between them, minimum wire width, minimum wire pitch etc. Hence, DRC cleaning is done to ensure the=at the routes can be fabricated and printed in silicon faithfully.
 
Signal short is also one of the critical issues as it causes functionality failure. It can be eliminated by moving the route to next layer with vias. This can lead to more DRCs (via width, via spacing, higher metal layer must be wider than lower metal layer etc.).
![Screenshot 2024-03-30 113826](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/f2eebef5-11ae-4803-a860-013947cfcb95)
![Screenshot 2024-03-30 114047](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/5a5ac979-93b7-4731-abf5-2395c9fadf29)


 
 
  
 
Power Distribution Network and routing
Lab steps to build power distribution network
1.	Go to openlane directory
2.	docker
3.	./flow.tcl -interactive
4.	package require openlane 0.9
5.	prep -design picorv32a -tag 19-03_16-40 (this is the folder till cts has been done)
6.	echo $::env(CURRENT_DEF) /openLANE_flow/designs/picorv32a/runs/19-03_16-40/results/cts/picorv32a.cts.def
7.	To generate PDN: gen_pdn
 
 
Lab steps from power straps to std cell power
The power and ground rails have a pitch of 2.72um and hence the reason reason why the custom inverter cell has a height of 2.72um, else the power and ground rails will not be able to power the cell. Looking at the LEF file runs/[date]/tmp/merged.lef, it is noticed that all cells are of height 2.72um and only width differs.
As shown below, power/ground pads -> power/ground ring-> power/ground straps -> power/ground rails to power up the standard cells.
![WhatsApp Image 2024-03-30 at 8 07 07 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/42075982-0aff-4f42-85da-49bb67e04b90)

 
Basics of global and detail routing and configure TritonRoute
TritonRoute is the engine that is used for routing. run_routing command does routing in OpenLANE.
![WhatsApp Image 2024-03-30 at 8 06 21 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/ed6f4853-79e3-4646-815c-2b73da367ab0)
![WhatsApp Image 2024-03-30 at 8 06 39 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/94e1a3b5-7d47-4d43-bad4-0228171b048a)


 

 
 
 
In the VLSI flow, the routing stage is highly critical and can be executed using either open-source or commercial tools. This stage is divided into two phases:
1.	Global Route / Fast Route:
o	This is accomplished using fast routing techniques where the area to be routed is partitioned into tiles or rectangles. Global routing establishes the initial framework for routing paths.
2.	Detail Route:
o	This phase involves meticulous tracking routing techniques to complete the routing process. Detailed routing fine-tunes and finalizes the paths to ensure proper connectivity and compliance with design constraints.
TritonRoute features
TritonRoute feature 1 - Honors pre-processed route guides:
M1 preferred direction is vertical and M2 preferred direction is horizontal. Whenever the tool encounters a non preferred direction route, then it divides the route into unit width. This is called splitting. The divided unit width sections that fall in the same line of preferred direction routes are merged. The edges which are parallel to the preferred routing direction are bridged with the upper layer, process caled as bridging. Non preferred routing guides are now converted into preferred routing guides of M2.
![WhatsApp Image 2024-03-30 at 8 07 37 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/ccc6919e-c034-4208-977a-5ee95ab4be9a)

 
 
TritonRoute feature 2 - Inter-guide connectivity:
M1 and M2 are connected at the purple colour areas. The tool will understand that there is overlap area, then it will add via to connect M1 & M2.
![WhatsApp Image 2024-03-30 at 8 07 52 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/a456af2e-46fa-480e-bc4a-2a9d343ebdb0)

 
 
TritonRoute feature 3 - intra- & inter-layer routing:
The preferred direction of the M1 layer is vertical, resulting in lines oriented vertically. The dashed lines are referred to as panels, with each routing guide assigned to a specific panel. When routing occurs within even-index panels, it's termed as intra-layer parallel panel routing. Initially, routing takes place simultaneously in all even-index panels, followed by routing in odd-index panels. This routing remains confined within a particular layer. Routing progresses from lower to upper layers, ensuring the orderly flow of routing operations.
![WhatsApp Image 2024-03-30 at 8 08 11 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/38a78166-611b-4046-8c80-ae605a3dcb43)

 
TritonRoute method to handle connectivity
![WhatsApp Image 2024-03-30 at 8 08 26 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/b65f3aea-57e6-4f6a-a055-9960b1414058)
![WhatsApp Image 2024-03-30 at 8 08 44 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/2a8e4fdb-9df2-4a6d-b440-c3abdd70249a)


 
 
 
The Goal of MILP (Mixed Integer Linear Programming) algorithm is to find the optimal solution to connect two Access point cluster.
![WhatsApp Image 2024-03-30 at 8 09 04 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/d97f8b31-24e4-4ea8-a043-360aa6937756)

 
 
In the above algorithm, for each access point, cost is found. Then, a minimum spanning tree between access points and cost. So, the algorithm says that minimal and most optimal point is nedded between two APCs.
Final files list post-route
With run_routing command, routing got completed. Both global routing (fast routing) and detail routing are done. It takes multiple iterations to bring down the DRC violations to 0. routing strategy was set to 0. In the intial iteration, the violation count was close to 25000 and at the 34th iteration, the violations got resolved and became 0. The entire routing operation took nearly 25 minutes.
![WhatsApp Image 2024-03-30 at 8 09 26 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/d21fb4bc-19c7-4120-8c33-e1663dd411b8)
![WhatsApp Image 2024-03-30 at 8 09 44 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/e2f62bf8-5124-4170-b40c-b7dd2a11e7d3)
![WhatsApp Image 2024-03-30 at 8 09 57 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/00e9c873-396f-4fd7-af65-b96f6f86a90c)



 
   
A DEF file will be formed in runs/[date]/results/routing/picorv32.def. Open the DEF file of routing stage in Magic.
![WhatsApp Image 2024-03-30 at 8 10 12 PM](https://github.com/ngs-chipdesign/vsdiat-report/assets/163662557/d6027b9a-076b-4ab5-b893-bc3835777249)

 
 
 
Parasitic extraction:
OpenLane does not have any spef extraction tool, so we use a separate tool present in work/tools/ directory.
1.	Go to /home/vsduser/Desktop/work/tools
2.	Inside that there is a folder named SPEF_EXTRACTOR
3.	SPEF_EXTRACTOR contains a list of files, out of which there is a python file called main.py. It helps to generate the SPEF provided there are lef & def files
4.	To create SPEF file python3 main.py /home/vsduser/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/26-03_05-49/tmp/merged.lef /home/vsduser/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/26-03_05-49/tmp/routing/picorv32a.def
5.	spef will be saved in the same location as def file. /home/vsduser/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/26-03_05-49/tmp/routing
 
The last stage will be to extract the GDSII file ready for fabrication run_magic
This uses Magic to stream the GDSII file runs/26-03_05-49/results/magic/picorv32a.gds. This GDSII file can then be read by Magic:
 
The PnR flow is done







 
