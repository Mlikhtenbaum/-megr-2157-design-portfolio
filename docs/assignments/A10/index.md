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

Choosing the smallest available lead screw (1/4" major diameter) from McMaster-Carr is more than adequate, as proven by the following formula that calculates the minor diameter of a 1/4" screw and compares it to our calculated minimum diameter of .0957". Therefore, recalculating stress values for our chosen 3/8"-12 lead screw is unnecessary, as it is even more capable of sustaining the applied forces.

This calculation proves that a 1/4"-16 screw has a minor diameter larger than our minimum calculated diameter: $$d_r = d - p = 0.2500'' - 0.0625'' = 0.1875'' > 0.0957''$$

<img width="2554" height="3295" alt="Min D" src="https://github.com/user-attachments/assets/038ba5b0-b299-46f9-b838-fcc27ffc2559" />
[Minimum diameter of lead screw]


#### Range of rotational speed given the linear speed:

Initially assumed a lead of .063" to match the smallest diameter alloy steel lead screw sizes provided by McMaster-Carr. After re-designing around a 3/8"-12 lead screw, our actual, final RPM ranges from .47 to 23.62.

<img width="2185" height="2926" alt="RPM" src="https://github.com/user-attachments/assets/d57c89f6-d824-45c4-95c5-2e5fd8db85f2" />
[Rotational speed of 1/4"-16 lead screw]

<img width="1971" height="1684" alt="Rpm recalc" src="https://github.com/user-attachments/assets/5c8e7f07-94e7-4421-9128-7257371db3c4" />
[Rotational speed of 3/8"-12 lead screw]


#### Select a lead screw by determining max torque to provide 2 kN tension to the test sample.

Determine the torque required to create 1 kN axial force per lead screw. The "Extra" note on the bottom uses the calculated torque value to determine the resultant shear, demonstrating that it is far below the typical shear yield threshold of steel (~35000 Psi).

<img width="1108" height="1419" alt="Torque og" src="https://github.com/user-attachments/assets/f6cdf30d-6ec6-42de-a814-bc77cf21105e" />
[Torque of 1/4"-16 lead screw]

<img width="1550" height="2658" alt="Torque recalc" src="https://github.com/user-attachments/assets/0151fb5c-f237-44b9-98d8-2afed25c62ea" />
[Torque of 3/8"-12 lead screw]

 
#### Select the leadscrew from the resources section on Leadscrews.

After conducting the aforementioned calculations, we initially selected the smallest leadscrew (alloy steel) offered by McMaster-Carr. It was the Alloy Steel Acme Lead Screw, Right Hand, 1/4"-16 Thread Size. Although that specific lead screw was capable of withstanding the applied load, the 1/4-16 nut that McMaster-Carr has available did not, so we had to recalculate our lead screw measurements. After recalculating, we chose to use an ACME 3/8"-12 lead screw, which has a larger diameter and therefore a larger inner thread bearing area. The required length will be determined by overall tensile tester geometry and possibly deflection calculations. We did not choose the ACME stub-thread design because those threads are meant for applications in which maintaining the wall thickness of a thin-walled sleeve is necessary (not relevant to our design).

Any of the lead screws in the following figure are possible choices:
<img width="1129" height="86" alt="list of compatible 38_12 lead screws" src="https://github.com/user-attachments/assets/e8453bc0-88b1-4297-93be-fd3b45e1084d" />
[3/8"-12 lead screws of varying lengths]

<img width="905" height="382" alt="38 Lead Screw Diagram" src="https://github.com/user-attachments/assets/0e868820-c0f6-45ab-91df-aa4e4dd5037b" />
[3/8"-12 lead screw dimensions drawing sourced from [site](https://www.mcmaster.com/93420A882/)]


### Nut and Flange Design (10pts): Misha
Analyze the internal threads of the nut to select a proper bronze nut/flange. Verify the internal threads support the load using the thread-bearing bending stress analysis in lecture notes and a safety factor.

This section of the project is where our design had to be altered, and calculations had to be redone. Our initial choice of the 1/4-16 lead screw was valid in terms of axial load, but the nuts available to us were incapable of sustaining our safety factor of 4.0. Therefore, we went back and decided to use a 3/8"-12 lead screw, allowing us to employ a taller nut that had more thread engagement, better distributing the applied loads.

Before redesign (using the 1/4"-16 screw), our safety factor was too low:$$SF_{\text{actual}} = \frac{\sigma_{B,\text{allow}}}{\sigma_B} = \frac{2,500\text{ psi}}{1,046.8\text{ psi}} = \mathbf{2.39}$$

After redesign (using the 3/8"-12 screw), our safety factor was more than adequate:$$SF_{\text{actual}} = \frac{\sigma_{B,\text{allow}}}{\sigma_B} = \frac{2,500\text{ psi}}{490.7\text{ psi}} = \mathbf{5.10}$$

<img width="2326" height="3007" alt="Nut stress" src="https://github.com/user-attachments/assets/9681a223-ac52-4a6d-8462-e97a776f9057" />
[Nut bearing stress calculation and recalculation]

The final flange nut we selected, based on its resultant safety factor, was the 932 Bearing Bronze Acme Flange Nut, Right-Hand, 3/8"-12 Thread Size (7/8" height), which has a serial number of 95120A592.

<img width="1002" height="766" alt="38 lead nut" src="https://github.com/user-attachments/assets/929b9d45-375a-47c6-aa74-52afe7c0b39b" />
[3/8"-12 lead nut dimensions drawing sourced from [site]([https://www.mcmaster.com/93420A882/](https://www.mcmaster.com/95120A592/))]


### Design the Crosshead (25 pts): Misha

Analyze the minimum strength required for the load and the maximum deflection of .1 mm. There is much freedom to design the crosshead to determine the size and material. Use research to determine an appropriate length of the crosshead. Use the nut flange to determine the minimum base.

To keep hand calculations relatively straightforward, we used a rectangular cross-section for our crosshead. 1060-H12 aluminum is to be the crosshead material, due to its high strength-to-weight ratio.

For length, engineering reasoning was used to determine a valid dimension. We needed our tensile tester to have a small enough footprint to sit on a regularly sized desk, but we also required a width with enough to allow adequate room for our dogbone test specimen and our lead screws, plus any additional clearance between components. The following diagram details the general measurements used to find our overall length, and the shear and moment diagrams that outline the behavior of the beam under loading.

<img width="2484" height="3203" alt="Crosshead general dimensions" src="https://github.com/user-attachments/assets/334f4b2e-e78b-4d69-aaa7-2d50676d283b" />
[General crosshead structure]

Although the overall length of the crosshead is 11in (updated from the initial length estimate of 10in found in figure "General crosshead structure"), only the middle 6in portion of it is affected by the applied forces, and therefore is the section analyzed in our calculations.

#### Use simple beam stress/strength analysis to determine the size and material of the crosshead.

<img width="2319" height="2995" alt="Crosshead beam stress" src="https://github.com/user-attachments/assets/eebdeaf4-97a8-4675-852e-734a373ace0a" />
[Height calculations from stress analysis]


#### Use simple beam deflection analysis to determine the size and material of the crosshead.

<img width="2607" height="3418" alt="Crosshead beam defl" src="https://github.com/user-attachments/assets/c40f0e88-c11d-41e5-898e-cfdaae2f8c59" />
[Height calculations from deflection analysis]

#### Crosshead final dimensions: 11in long, 1.25in x 1.25in cross section

Based on an assumed base dimension of 1.25in, our crosshead needs to have a height of 1.091in to resist the stress created by the applied loads. However, since this height is not limited by our design constraints, using a 11in long, 1.25in x 1.25in piece of aluminum bar stock will simplify any further calculations, and ensure that sourcing components will be a simple process.


#### Generate a multiview paper sketch of the tensile tester crosshead. 

The sketch should be neatly presented with appropriate views (front, top, side) and sufficient annotations to communicate geometry, proportions, and nut/flange mounting intent.

For this multiview sketch, the overhanging portions of the crosshead that mate with the alignment columns on the outside of the tester have been upped to 2in past each flange. This may be altered once we create the overall structure of the tensile tester in CAD, but the overhanging portion of the structure is totally unaffected by the applied forces regardless.

<img width="2689" height="2151" alt="Crosshead multiview sketch" src="https://github.com/user-attachments/assets/c6c33474-f9ed-494d-927e-dd1c52876c39" />
[Crosshead multiview sketch]


### Tabulating Costs (10 pts): Misha
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

### 2157 Addition: Create a detailed drawing of the crosshead with a proper title block (20 pts): Ryan
Produce a multi-view CAD drawing of the crosshead with complete dimensioning and proper tolerancing.


## Decide


We decided that Misha would complete the hand calculation portion of this project, while Ryan would complete the 3D modelling and assembly sections. 



## Communicate


Lessons learned:
