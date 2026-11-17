# A11 – Motor Selection

## Objectives:

Part 2 Scope of Work:
Select a Motor
Design Motor Mounts
Select or design a coupler
Design a Frame to support a crosshead stability and tensile load
Select or design a Clamp Analysis and Design
Provide complete CAD model of the engineered parts of the Tensile Tester
Deliver a Bill of Materials and Engineering Cost

## Analyze:


### Motor Selection and Attachments:

(10pts) Use torque and speed requirements derived from the lead screw design to select an appropriate motor (DC, stepper, or gearmotor). Document all relevant motor parameters: rated torque, speed, efficiency, voltage/current, and mounting interface. Verify that:

- The motor provides sufficient output torque to achieve the maximum 2 kN load across the entire speed range (1–50 mm/min).
- Provide a speed torque curve showing the selected motor.

(10pts) Design a motor mount bracket or housing to securely attach the motor to the tester frame. Use the mounting holes in the motor as a pattern for features in the bracket. Select a four hole pattern to secure the mount to the top of the frame.  The mount must: a. ) Maintain precise alignment with the lead screw to prevent binding or eccentric loading. b. Accommodate service access for assembly and maintenance. c.) Withstand both operational torque and reaction forces without excessive deflection.

- List all the knowns and unknowns.
- Detail a FBD for the bearing stress.
- Model the equations to solve for thickness.
- Numerically solve for the minimum thickness.

(10pts) Select/design a coupler to connect. Use shear stress torsion analysis to determine the inner and outer diameter of the coupler.

- List all the knowns and unknowns.
- Detail a FBD for the torsional stress
- Model the equations to solve for thickness.
- Numerically solve for the thickness.

### Analyze and design a Frame

(10pts) Analyze the affected twist by the motors to design a bracket to affix the vertical standoffs of the frame to the top of the frame. Select proper Connectors for T-Slot Framing using the resources.

- List all the knowns and unknowns.
- Detail a FBD for the top of the frame
- Symbolically represent the forces required to stabilize the top of the frame at the ends.
- Using the appropriate stress analysis select the proper mounting from the top to the vertical frame.

(20 pts) Verify the top of the frame constructed from heavy 40 Series will provide the strength necessary to hold the loads of the lead screw load and torque. Conduct an FEA using the proper constraints and loads.

- Model Setup: Define boundary conditions: constrain interfaces to frame brackets and motor brackets. Apply loading that represents two the 1 kN axial tension path through the leadscrew and the two moments applied from the motor.
  
- Meshing & Verification: Use a solid mesh with local refinement at stress raisers. Perform a mesh convergence check and report key metrics.
  
- Results to Report:
  - Maximum von Mises stress and location.
  - Maximum vertical deflection at the grip line.
  - Factor of Safety (based on chosen material yield).
  - Brief discussion of load path and any observed twisting/warping tendencies.
    
- Optimization Pass:
  - Propose targeted changes (e.g., pocketing, ribbing, thicker flange pads, larger fillets).
  - Any shift in critical locations.

(20 pts) Verify the vertical components of the frame constructed from heavy 40 Series will provide the strength necessary to hold the loads of the lead screw load and torque. Conduct an FEA using the proper constraints and loads. Note: there should be two forces, one axial compression and one transverse load.

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

(10pts) Design a mounting bearing which allows the end of the leadscrew to rotate using a RC3 Fit class and affix to the bottom of the frame. Clearance holes for bolts must be researched in the Machinery’s Handbook.
Justify each size and location dimension of the mount.
Note the functional tolerances for the appropriate dimensions.

### Bill of Materials and Labor Costs

(10pt) Tabulate all the costs associated with both assignment parts. Use the following template to show the associated costs. You are to use an entry level mechanical engineering designer cost per hour of $35/hour.

## Decide: 

Reference your concept selection (Pugh matrix) here. How does this design follow from that decision?_

## Communicate:
