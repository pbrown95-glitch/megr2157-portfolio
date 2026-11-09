# A9 – Pulley System

## Objective 

-Design the belt drive: determine tight- and loose-side tensions, calculate the required belt area and diameter, determine circumference, and select suitable belting.

-Size the shafts: select a heat treatment for 1060 steel and calculate the minimum shaft area and diameter needed to transmit torque.

-Design the journal bearings: calculate bearing pressure, surface speed, and the resulting PV, then determine dimensions and select a suitable material.

-Design the supporting frame: establish dimensions and an arrangement that supports the bearings and maintains shaft alignment.

-Document the engineering process: present knowns, unknowns, assumptions, free-body diagrams, symbolic equations, numerical results, and specific lessons learned.


## System Design

### Belt

The belt drive was designed using two 3-inch pulleys with a center distance of 5 inches, an operating speed of 1500rpm, and a static tension of 5lb in the belt. An assumed coefficient of friction of 1 and a wrap angle of 180 degrees, or pi radians. Applying the capstan equation at impending slip and assuming T1=T2=2To produced a tight-side tension of 9.586 lbf and a loose-side tension of 0.414 lbf. Using the given material for the belt, polyurethane, and its yield strength of 471 and a safety factor of 3, the minimum belt area was calculated as 0.279 inches. A 5/16-inch polyurethane round belt, McMaster-Carr part 59725K733, was selected. Its calculated axial-stress safety factor is 3.77, and its minimum permitted pulley diameter of 2.5 inches is below the specified 3-inch diameter.

![w](InputKnowns.png)

### Shafts

The shafts were modeled as solid circular members transmitting steady torque. The difference between the belt tensions produces a transmitted torque of 13.76 lbf-in. Quenched-and-tempered AISI 1060 steel was selected, using an adopted tensile yield strength of 580 MPa, or approximately 84.1 ksi. Using the maximum shear stress criterion and a safety factor of 3, the minimum shaft cross-sectional area was calculated as 0.02296 square inches. This corresponds to a minimum diameter of 0.171 inches.

![w](InputKnowns.png)

### Journal Bearings

Each shaft was supported by two journal bearings. The total radial belt load of 10 lbf therefore produces a load of 5 lbf per bearing. A bearing length of 0.300 inches was selected, using the calculated shaft diameter of 0.171 inches. The projected bearing area was 0.0513 square inches, giving an average pressure of 97.47 psi. At 1500 rpm, the shaft surface speed was 67.15 ft/min, producing a PV value of approximately 6545 psi·ft/min. Porous bronze was selected from Table 4. Its listed pressure, surface-speed, and PV limits exceed the calculated operating values. The PV limit is approximately 7.64 times the operating value.

![w](InputKnowns.png)

### Support Frame

With no specific use designated for this pulley system, an effective support frame is not possible, and I was left to design this as I felt fit. Below you will find a simple housing sketch for the pulleys so they are held in place and the forces applied do not cause a misaligned belt. 

![w](InputKnowns.png)

## Lessons Learned

This assignment showed me that belt tension performs two different functions in a power transmission system. The difference between the tight- and loose-side tensions produces torque, while their sum produces the radial load carried by the shafts and bearings. I also learned to distinguish calculated minimum dimensions from selected design dimensions and to identify which loading conditions each calculation actually verifies. This assignment took me about 3 hours. 

