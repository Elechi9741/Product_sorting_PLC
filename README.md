# Product_sorting_PLC
This is a PLC program to sort products on a production line
SOFTWARE USED: Siemens TIA Portal
CONTROLLER: S7 1500
The working prtinciple of the program is described below
The conveyor has two velocities, normal and low, in addition, to reverse, controlled by three different signals. When measuring the product length, the belt moves at normal velocity.
Short product: The product is transported forward to photocell FC4. Then the conveyor speed drops to low, and when the product reaches FC5, the conveyor is stopped. The product is then pushed off the conveyor belt by a pneumatic piston. 

The end positions of the piston are detected by two sensors, G1 and G2. When the piston has returned to its rear position, the cycle ends.
Medium product: The product continues forward to photocell FC5, which marks the end of the cycle. (It is assumed that the product falls off the belt before a new product passes
FC1.)

Long product: The conveyor stops for 2 seconds and is then reversed. When the product again passes FC1 (on the return), the conveyor shall continue in the backward direction in a further 5 seconds. It is then assumed that the product has dropped off the conveyor belt and the cycle ends.
