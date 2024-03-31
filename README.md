Advanced Physical Design using Openlane/Sky130
Contents:
1.	Inception of open-source EDA, OpenLANE and Sky130 PDK
     o	How to talk to computers?
         	Introduction to QFN-48 Package, chip, pads, core, die and IPs
         	Introduction to RISC-V
         	From Software Applications to Hardware
     o	SoC design and OpenLANE
         	Introduction to all componenets of open-source digital asic design
         	Simplified RTL2GDS flow
         	Introduction to OpenLANE and Strive chipsets
         	Introduction to OpenLANE detailed ASIC design flow
     o	Getting familiar to open-source EDA tools
         	OpenLANE Directory structure in detail
         	Design Preparation Step
         	Review files after design prep, run synthesis, and characterize synthesis results
2.	Good floorplan vs bad floorplan and introduction to library cells
     o	Chip FLoor planning considerations
         	Utilization factor and aspect ratio
         	Concept of pre-placed cells
         	De-coupling capacitors
         	Power Planning
         	Pin placement and logical cell placement blockage
         	Steps to run floorplan using OpenLANE and view floorplan layout in Magic
    o	Library Binding and Placement
         	Netlist binding and initial place design
         	Optimize placement using estimated wire-length and capacitance
         	Congestion aware placement using RePlAce
    o	Cell design and characterization flows
    o	Timing characterization
3.	Design library cell using Magic Layout and ngspice characterization
    o	Labs for CMOS inverter ngspice simulations
         	IO placer revision
         	SPICE deck creation and simulation for CMOS inverter
         	Switching Threshold Vm
         	Static and dynamic simulation of CMOS inverter
         	Lab steps to gitclone vsdstdcelldesign
o	Inception of Layout CMOS fabrication process
o	Lab introduction to Sky130 basic layers layout and LEF using inverter
o	Sky130 Tech File Labs
4.	Pre-layout timing analysis and importance of good clock tree
o	Timing modelling using delay tables
	Lab steps to convert grid info to track info
	Lab steps to convert magic layout to std cell LEF
	Introduction to timing libs and steps to include new cell in synthesis
	Delay tables
	Lab steps to configure synthesis settings to fix slack
o	Timing analysis with ideal clocks using openSTA
	Setup timing analysis and introduction to flip-flop setup time
	Introduction to clock jitter and uncertainty
	Lab steps to configure OpenSTA for post-synth timing analysis
	Lab steps to optimize synthesis to reduce setup violations
o	Clock Tree Synthesis TritonCTS and signal integrity
	Clock tree routing and buffering using H-Tree algorithm
	Crosstalk and clock net shielding
	Lab steps to run and verify CTS using TritonCTS
o	Timing analysis with real clocks using openSTA
	Setup timing analysis using real clocks
	Hold timing analysis using real clocks
	Lab steps to analyze timing with real clocks using OpenSTA
	Lab steps to execute OpenSTA with right timing libraries
5.	Final steps for RTL2GDS using tritonRoute and openSTA
o	Routing and design rule check (DRC)
	Introduction to Maze Routing
	Design Rule Check
o	Power distribution network and routing
	Lab steps to build power distribution network
	Lab steps from power straps to std cell power
	Basics of global and detail routing and configure TritonRoute
o	TritonRoute features
	TritonRoute method to handle connectivity
	Final files list post-route

