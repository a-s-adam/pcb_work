Working with JDM product development structures, it's hard to get full exposure on an entire electrical PCB design from start to finish. The goal of this repository is to display design, component selection, schematic capture, layout, ordering, and bring-up without sharing designs done during my 9-5 job.


dev_board
ATMEGA
- ATMEGA32L8A : http://ww1.microchip.com/downloads/en/DeviceDoc/doc2503.pdf
- Info on Pi Filter (used to filter 3.3V for analog components : https://resources.altium.com/p/pi-filter-circuit-design-formulas-and-calculator 
- JTAG pinout Overview: https://www.xjtag.com/about-jtag/jtag-a-technical-overview/
- [Work in Progress]

MixSigBoard
- STM32 Based board with 2 SPI interfaces (ADC,DAC), ADC input, DAC output, a few GPIO's via RGB LED's, and Software Debug (SWD) interface.
- Analog Bias Generator, anti-aliasing filters, power supply line filtering, USB-C 2.0 compatibility
- Ground via next to all signal vias to give short return path and reduce EMI
- Fan out of traces where possible to reduce cross talk
- PHYSICAL separation of analog and digital components (placing A&D components far apart from each other has best results of reducing noise between the two) https://www.youtube.com/watch?v=ySuUZEjARPY
- Stitching Vias placed throughout board (2.5 mm grid)
- Silkscreen labeling of circuit portions
- Included Gerber, BOM, footprints,symbols, drill files

FPGA_Board
- AMD Zynq-7000 based board: https://docs.amd.com/v/u/en-US/zynq-7000-product-selection-guide [XC7Z010-2CLG400I]
- Config Memory is determined by FPGA chosen: https://docs.amd.com/r/en-US/ug908-vivado-programming-debugging/Virtex-UltraScale-Configuration-Memory-Devices?tocId=SfnAO9Qdpk7bcqPQwSsYiQ
- BGA Routing Application Manual: https://docs.amd.com/r/en-US/ug1099-bga-device-design-rules/Introduction
- Stack-up Selection for Various Layer PCB's https://www.pcbway.com/multi-layer-laminated-structure.html
- [Work in Progress]
