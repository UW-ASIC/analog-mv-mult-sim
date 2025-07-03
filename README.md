Purpose
=======

* Verilog-A and Python simulations of the system to help us determine the specs
    * Input voltage range / operating zones for the PMOS resistors
    * Required quantization levels for DACs and ADCs
* No need to go into detailed implementation of each block, only a functional model is needed
* By understanding the specs we can make a better choice about the specific architecture for each block

Verilog-A
=========

* Each block can be a functional description of how the block should operate
* Non-idealities can be introduced by either instantiating SPICE components in xschem, or by modelling them in the verilog-a
* System testbenches can be made in SPICE

File Structure
--------------

src
    top.va
    module_name
        top.va
        other files.va
        module_tb.va or module_tb.sch
tb
    transient_sim_tb.sch
    ac_sim_tb.sch

Python
======

* High level functional model of each block
* Good for simulating impact of quantization and other basic non-idealities
