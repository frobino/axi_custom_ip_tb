axi_custom_ip_tb
================

A testbench for an axi 4 lite custom slave IP. 

I was going through the "Zynq Book" tutorials. 
One of them shows how to create a custom hdl peripheral driving LEDs, 
and how to connect it to the Zynq PS through axi lite. 
The tutorial is called something like "led_controller_1.0". 

The main problem of the tutorial is that it does not show how 
to do a behavioural simulation of the system (i.e. the classical 
modelsim/xsim simulation with waveforms, showing how the PS communicates 
through axi to the custom pheriperal implemented in PL). 

This is because at the moment seems very difficult to simulate 
Zynq PS and PL in a behavioural simulation at the same time. 

This project shows how it is possible to debug separately from the 
Zynq PS a custom IP implemented in the PL. 
It takes the same exact example generated thorugh the "Zynq Book" 
tutorial, and includes a testbench which generates WRITE and READ 
in axi format.  

TODO
================

- check the "example_designs" folder of the ip generated through the 
  Zynq Book. It includes tcl files to automatically create write and 
  Read master transactions and test the custom IP.