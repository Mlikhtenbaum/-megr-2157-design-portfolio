# A11 – Motor Selection

## Objectives:

Part 2 Scope of Work:
Select a Motor
Design Motor Mounts
Select or design a coupler
Design a Frame to support crosshead stability and tensile load
Select or design a Clamp Analysis and Design
Provide a complete CAD model of the engineered parts of the Tensile Tester
Deliver a Bill of Materials and Engineering Cost

## Analyze:


### Motor Selection and Attachments: 

(10pts) Use torque and speed requirements derived from the lead screw design to select an appropriate motor (DC, stepper, or gearmotor). Document all relevant motor parameters: rated torque, speed, efficiency, voltage/current, and mounting interface. Verify that: *Misha*

A useful source for understanding how T-slot rail hardware functions can be found [here](https://8020.net/blog/guide-to-industrial-fasteners-for-t-slot-framing.html)

- The motor provides sufficient output torque to achieve the maximum 2 kN load across the entire speed range (1–50 mm/min).
- Provide a speed-torque curve showing the selected motor.

Based on the following hand calculations, the "Stepper Motor with Square Body, NEMA 23, 173.5 in.-oz. Maximum Holding Torque (SN: 6627T53)" from McMaster-Carr can provide an adequate amount of torque (when assuming an ACME lead screw efficiency of 30%) to create 1KN of force per lead screw. The motor specifications can be accessed at this [link](https://www.mcmaster.com/6627T53/)

<img width="2073" height="1634" alt="Motor Selection" src="https://github.com/user-attachments/assets/a30ff62f-08ef-40b5-bf3d-343fafbeb96d" />
[Hand calculations for torque conversion and thread efficiency]

<img width="627" height="477" alt="Stepper Motor Image" src="https://github.com/user-attachments/assets/63db5a08-6417-4a33-9222-4a95cd20463f" />
[Chosen stepper motor]

<img width="627" height="477" alt="Stepper Motor Drawing" src="https://github.com/user-attachments/assets/babe5154-d9ac-41ea-a854-e51e1fc14f1b" />
[Chosen stepper motor drawing]

<img width="1007" height="758" alt="Stepper Motor Speed Torque Curve" src="https://github.com/user-attachments/assets/178c7923-04f0-4e7b-b0d0-47e95ade5858" />
[Chosen stepper motor speed-torque curve]

(10pts) Design a motor mount bracket or housing to securely attach the motor to the tester frame. Use the mounting holes in the motor as a pattern for features in the bracket. Select a four-hole pattern to secure the mount to the top of the frame. The mount must: a.) Maintain precise alignment with the lead screw to prevent binding or eccentric loading. b.) Accommodate service access for assembly and maintenance. c.) Withstand both operational torque and reaction forces without excessive deflection. *Misha*

The T-slot nuts we will use to couple the motor mount to the T-slot rails can be found [here](https://8020.net/40-3203.html).

An important consideration to take into account during this phase of the design was ensuring that the motor mounting bracket and the load cell have enough clearance to fit within the constraints of our current frame setup. This check is detailed in the calculation: ((.5125 * 2) + 2.25) + 2.4, which adds up to 5.675 in (which is less than 6 in), meaning that the current motor mount design will work with our current frame spacing.

- List all the knowns and unknowns.
- Detail a FBD for the bearing stress.
- Model the equations to solve for thickness.
- Numerically solve for the minimum thickness.

When solving for tear-out thickness in the following calculations, L is simplified to be the distance from the edge of the hole to the nearest edge of the bracket, rather than the distance from the edge of the hole to the bracket edge along the path of the force vector. This aids in ease of calculation and increases the resultant safety factor of the design in vulnerable areas.

After conducting our calculations, a minimum thickness of .0054 in was determined. This dimension may resist the applied force on paper, but would not function in any real application; therefore, our bracket will be made of 1/16 in thick 6061-H12 Plate.

<img width="2086" height="2989" alt="Force Calculation" src="https://github.com/user-attachments/assets/403b2bcd-6180-44eb-84e1-82c859f5472a" />
[Motor mounting and motor hole force calculations]

<img width="2358" height="1530" alt="Thickness Determination" src="https://github.com/user-attachments/assets/7a324c7c-99c7-48fe-9242-773e1b4cfc24" />
[Resultant thickness calculations]

(10pts) Select/design a coupler to connect. Use shear stress torsion analysis to determine the inner and outer diameter of the coupler. *Misha*

- List all the knowns and unknowns.
- Detail an FBD for the torsional stress
- Model the equations to solve for thickness.
- Numerically solve for the thickness.



### Analyze and design a Frame

(10pts) Analyze the affected twist by the motors to design a bracket to affix the vertical standoffs of the frame to the top of the frame. Select proper Connectors for T-Slot Framing using the resources. *Misha*

- List all the knowns and unknowns.
- Detail a FBD for the top of the frame
- Symbolically represent the forces required to stabilize the top of the frame at the ends.
- Using the appropriate stress analysis, select the proper mounting from the top to the vertical frame.

(20 pts) Verify that the top of the frame constructed from heavy 40 Series will provide the strength necessary to hold the loads of the lead screw load and torque. Conduct an FEA using the proper constraints and loads. *Ryan*

- Model Setup: Define boundary conditions: constrain interfaces to frame brackets and motor brackets. Apply loading that represents two of the 1 kN axial tension paths through the leadscrew and the two moments applied from the motor.
  
- Meshing & Verification: Use a solid mesh with local refinement at stress risers. Perform a mesh convergence check and report key metrics.
  
- Results to Report:
  - Maximum von Mises stress and location.
  - Maximum vertical deflection at the grip line.
  - Factor of Safety (based on chosen material yield).
  - Brief discussion of load path and any observed twisting/warping tendencies.
    
- Optimization Pass:
  - Propose targeted changes (e.g., pocketing, ribbing, thicker flange pads, larger fillets).
  - Any shift in critical locations.

(20 pts) Verify the vertical components of the frame constructed from heavy 40 Series will provide the strength necessary to hold the loads of the lead screw load and torque. Conduct an FEA using the proper constraints and loads. Note: there should be two forces, one axial compression and one transverse load. *Ryan*

- Model Setup: Define boundary conditions: constrain interfaces to frame brackets and motor brackets. Apply loading that represents the two loads.
  
- Meshing & Verification: Use a solid mesh with local refinement at stress raisers. Perform a mesh convergence check (at least two refinements) and report key metrics (max von Mises stress and max vertical deflection).
  
- Results to Report:
  - Maximum von Mises stress and location.
  - Maximum vertical deflection at the grip line.
  - Factor of Safety (based on chosen material yield).
  - Brief discussion of load path and any observed twisting/warping tendencies.
    
- Optimization Pass:
  - Propose targeted changes (e.g., pocketing, ribbing, thicker flange pads, larger fillets).
  - Any shift in critical locations.

### Design Floating Bearing Mount

(10pts) Design a mounting bearing that allows the end of the leadscrew to rotate using an RC3 Fit class and affix to the bottom of the frame. Clearance holes for bolts must be researched in the Machinery’s Handbook. *Misha*

- Justify each size and location dimension of the mount.
- Note the functional tolerances for the appropriate dimensions.

### Bill of Materials and Labor Costs

(10pt) Tabulate all the costs associated with both assignment parts. Use the following template to show the associated costs. You are to use an entry-level mechanical engineering designer cost per hour of $35/hour. *Misha*


### 2157 Addition:

(30pts) Create a drawing package which includes detailed drawings of the designed components, an assembly isometric drawing, and a Bill of Materials (BOM). Note: include the crosshead drawing from the previous assignment.

- Each drawing has its proper title block.
- Apply ASME Y14.5 standards for dimensioning and tolerancing.
- Include the following:
- Third-angle projection layout.
- Tolerance block consistent with course standards:
  - X.X ± .02
  - X.XX ± .01
  - X.XXX ± .005


## Decide: 


We chose a stepper motor for our tensile tester because it can measure strain when connected to a microcontroller, allowing us to use Hooke's Law to determine the test material's modulus of elasticity.

Reference your concept selection (Pugh matrix) here. How does this design follow from that decision?


## Communicate:
