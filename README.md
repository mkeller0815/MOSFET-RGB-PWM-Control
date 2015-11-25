#MOSFET-RGB-PWM-Control
 ======================

## 1.0 About

A small controllerboard that can be used by microcrontrollers to control bigger loads with MOSFET drivers

## 2.0 Layout

![Layout] (https://github.com/mkeller0815/MOSFET-RGB-PWM-Control/raw/master/pcb_layout.png)

## 3.0 Usage

The board can be used to control DC voltage up to 55V on 3 different channels. 
There are 2 Terminal-Blocks (Pheonix) with 5mm (0.2 inch) spacing for the high-current part and 2.54 (0.1 inch) for the control part.

Connect the voltage you need to the both power connector pins, connect your microcontroller to the "control"-connector. Make sure that GND is also connected. 
You can drive the control-lines with static or pwm-signals. A high on a control-line switches the corresponding output-line to the applied voltage.

The copper traces should be able to handle up to 3 ampere of constant current per line. But in this case a heatsink should be mounted on the MOSFETs.  

## 4.0 Details

The board uses 3 IRLIZ44N N-channel MOSFETs to drive up to 55V and 3A an 3 channels. 

http://www.irf.com/product-info/datasheets/data/irliz44n.pdf

The gate of the MOSFET is pulled down to GND by a 10k resistor. 
