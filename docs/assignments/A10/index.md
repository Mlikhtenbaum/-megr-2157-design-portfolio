# A10 – Lead Screw Translating System


## Objective:


Design and build a mechanically driven tensile tester capable of applying up to 2 kN axial tensile load with a controllable crosshead speed from 1 to 50 mm/min. Each team is responsible for the mechanical components outlined below. The system will provide consistent, well-aligned loading for polymers and light metals, suitable for instructional use and basic materials evaluation.

Relevant Example Figures:

<img width="726" height="778" alt="Figure 1 Concept of Tensile Tester" src="https://github.com/user-attachments/assets/ab0eb70e-f2b4-464b-bc3c-611c4b7f3536" />
[Figure 1: Tensile Tester Concept]

<img width="560" height="407" alt="image" src="https://github.com/user-attachments/assets/3c3506c1-dddb-444b-814e-323babdee42b" />

[Figure 2: Tensile Tester Diagram found on page 15 of [this](https://repositum.tuwien.at/bitstream/20.500.12708/200949/1/Demmel%20Stella%20-%202024%20-%20Design%20manufacturing%20and%20testing%20of%20an%20open-source...pdf) reference document]


Part 1 Scope of Work
Develop a lead-screw–driven crosshead 
Ensure accurate, repeatable load application to 2 kN with minimal crosshead deflection and misalignment.
Provide robust specimen gripping, simple calibration provisions (mechanical), and safe, ergonomic operation.

Key Constraints
No electronics, no software: purely mechanical.
Load capacity: 2 kN (with appropriate safety factor in structure and drivetrain).
Speed range: 1–50 mm/min (achieved via screw lead selection).
Form factor: bench-top footprint favored; manageable overall height; 18-inch leadscrew minimum.
Safety Factor: 4


## Analyze:


### Leadscrew design (35pts): Misha

ASTM A193 Grade B7 steel (alloy steel) is used for the leadscrew material in order to minimize necessary dimensions. ASTM A193 Grade B7 steel has a tensile yield strength of 125000 Psi.

To select a leadscrew, the team must determine the minimum diameter, rotational speed range, and maximum torque.


#### Minimum diameter:

Choosing the smallest available lead screw (1/4" major diameter) from McMaster-Carr is more than adequate, as proven by the following formula that calculates the minor diameter of a 1/4" screw and compares it to our calculated minimum diameter of .0957". 

$$d_r = d - p = 0.2500'' - 0.0625'' = 0.1875'' > 0.0957''$$

<img width="2554" height="3295" alt="Min D" src="https://github.com/user-attachments/assets/038ba5b0-b299-46f9-b838-fcc27ffc2559" />


#### Range of rotational speed given the linear speed:

Assume a lead of .063" to match the smallest diameter alloy steel lead screw sizes provided by McMaster-Carr.

<img width="2185" height="2926" alt="RPM" src="https://github.com/user-attachments/assets/d57c89f6-d824-45c4-95c5-2e5fd8db85f2" />


#### Select a lead screw by determining max torque to provide the 2 kN tension to the test sample.

Determine neccesary torque application to create 1KN axial force per lead screw.

<img width="2547" height="3360" alt="Torque App" src="https://github.com/user-attachments/assets/f3c77a53-c0d0-49a8-bb2b-3010bf7eab54" />


#### Select the leadscrew from the resources section on Leadscrews.

The leadscrew we have selected after conducting the aforementioned calculations is the smallest one (of alloy steel) offered by McMaster-Carr. It is the Alloy Steel Acme Lead Screw, Right Hand, 1/4"-16 Thread Size. The required length will be determined by overall tensile tester geometry and possibly deflection caluclations. For reference, the serial number of a 6" long 1/4"-16 lead screw is 93420A881 on McMaster-Carr.


### Nut and Flange Design (10pts): Misha
Analyze the internal threads of the nut to select a proper bronze nut/flange. Verify the internal threads support the load using the thread-bearing bending stress analysis in lecture notes and a safety factor.




### Design the Crosshead (25 pts): Misha
Analyze the minimum strength required for the load and the maximum deflection of .1 mm. There is much freedom to design the crosshead to determine the size and material. Use research to determine an appropriate length of the crosshead. Use the nut flange to determine the minimum base.

#### Use simple beam stress/strength analysis to determine the size and material of the crosshead.

#### Use simple beam deflection analysis to determine the size and material of the crosshead.

#### Generate a multiview paper sketch of the tensile tester crosshead. 
The sketch should be neatly presented with appropriate views (front, top, side) and sufficient annotations to communicate geometry, proportions, and nut/flang mounting intent.


### Tabulating Costs (10 pts): Ryan
In order to get credit for this portion of the assignment, you must not use an image for the table, and it needs to have functional links. 


### Parametric Modeling (20 pts): Ryan
Download/create 3D models. Assemble the components in CAD. Do not create from scratch items you can download.

#### Crosshead (designed):

#### Leadscrew (downloaded):

#### Nut/Flange (downloaded):

#### Frame (parts downloaded):


### 2157 Addition: Use Finite Element Analysis (FEA) on the crosshead (20 pts): Ryan

#### Model Setup: 

#### Meshing & Verification:

#### Results to Report:

#### Optimization Pass:

### 2157 Addition: Create a detailed drawing of the crosshead with a proper title block (20 pts): Misha
Produce a multi-view CAD drawing of the crosshead with complete dimensioning and proper tolerancing.


## Decide


We decided that Misha would complete the hand calculation portion of this project, while Ryan would complete the 3D modelling and assembly sections. 

Our tensile tester will have a linear speed of 25mm/min.

Current Point Split: 90 Misha, 50 Ryan.


## Communicate


Lessons learned:
