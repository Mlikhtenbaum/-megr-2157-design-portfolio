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

ASTM A193 Grade B7 steel is used for the leadscrew material in order to minimize necessary dimensions. ASTM A193 Grade B7 steel has a tensile yield strength of 125000 Psi.

In order to select a leadscrew, the team must determine the minimum diameter, a range of rotational speed, and maximum torque.

#### Minimum diameter:

#### Range of rotational speed given the linear speed:

#### Select a lead screw by determining max torque to provide the 2 kN tension to the test sample.

#### Select the leadscrew from the resources section on Leadscrews.


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

Current Point Split: 90 Misha, 50 Ryan.


## Communicate


Lessons learned:
