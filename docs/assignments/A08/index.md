# A8 – Gearbox Design

## Objectives:

- Design a gearbox that can be assembled and disassembled.
- Analyze and size input and output shafts for strength.
- Design journal bearings to support shafts.
- Create a gearbox housing with proper clearance and fastening.
- Use parametric CAD modeling to generate a final design.
- Document calculations, sketches, and lessons learned.

## Analyze:



### Step 1: Shaft Calculations and Design Alterations:

- Use the equations for stress outlined in the lecture and Machinery’s Handbook to determine if the input and output shafts’ diameters are sufficient.

#### Input and Output Shaft Calculations:

- Calculations based on material information provided [here](https://matweb.com/search/DataSheet.aspx?MatGUID=d1844977c5c8440cb9a3a967f8909c3a)
- Safety factor of shafts was calculated to be 14.85 for input and 44.55 for output, both of which are more than acceptable. The current diameter of the shafts is adequate.

<img width="2333" height="3022" alt="Input output shaft calcs real" src="https://github.com/user-attachments/assets/a1286925-282f-4d67-b724-17af68eee142" />

<img width="760" height="395" alt="SF Determination for Shafts" src="https://github.com/user-attachments/assets/e23333c2-d650-4c7d-9a4e-291850b3cb75" />


### Step 2: Design Journal Bearings:

#### Journal Bearing Sizing:

 - Choose an appropriate size and length of the journal bearing, and determine the pressure, velocity, and PV rating
 - Use 2 input bearings with a length of .15625" (5/32") to account for the necessary amount of shaft sticking out of the gearbox (.36"), bearing contact length (.3125"), and gear length and clearance (.325").
 - Use 1 output bearing with a length of .375" (3/8") to account for the necessary amount of shaft sticking out of the gearbox (.24"), bearing contact length (.375"), and gear length and clearance (.385")

 - Input Shaft Bearing: Oil-Embedded 841 Bronze Sleeve Bearing for 1/8" Shaft Diameter and 3/16" Housing ID, 5/32" Long (6391K326). Resultant safety factor of 11.19 when considering the PV rating. *NOTE: These are the calculations for a scenario in which only one bearing is being used. In my gearbox design, I plan to employ two, which would double this safety factor.*

 - Output Shaft Bearing: Oil-Embedded 841 Bronze Sleeve Bearing for 1/4" Shaft Diameter and 5/16" Housing ID, 3/8" Long (6391K33). Resultant safety factor of 71.62 when considering the PV rating.

Hand Calculations:

#### Journal Bearing Thickness:

- Design the thickness of the journal bearings; ensure chosen bearing thicknesses match up, alter if not applicable.
- The calculated thickness for the input journal bearing was 7.93E-4" (0.000793"), while the output journal bearing thickness was calculated to be a minimum value of 3.31E-4 (0.000331"), both of which are satisfied by their current thicknesses (.032" for the output bearing and .0325" for the input).
- The chosen bearings (input 6391K326 and output 6391K33) are more than capable of handling the applied loads.

Hand Calculations:
  
### Step 3: Gearbox Sketch:

Gearbox Sketch:

### Step 4: Gearbox 3D Model:

- Where appropriate, parametrically generate critical features of a solid model starting with the known parameters and finishing with the dimensions and material.
- Download the necessary items from Mac-Master
- Generate the rest of the solid model.

#### Processes:

##### Box: 

The gearbox box is the back section of the gearbox in which the gears are actually contained.

1. Create an initial sketch, using square geometry to simplify the design. Estimate the inside width using the actual gear diameters to ensure ample clearance, and add .2" to provide at least .1" clearance on all inner faces of the box. Assume a thickness of .1" for the walls of the box.

##### Cover: 

The gearbox cover is the front cover that has holes for bolts that secure it to the rest of the gearbox. It also has two toleranced holes that the brass journal bearings are pressed into.

1. 

### MEGR 2157 Addition:

- Produce six multi-view CAD drawings and one assembly with complete dimensioning and proper tolerancing.
- At least two callouts for different tolerancing applied to critical features.

## Decide

- One decision I made initially was to have the longer segment of each shaft sticking out of the flanged side of its respective gear. This allows the longer shaft segment, which may experience bending forces, to resist them better.
- Another decision I made was to employ ASTM A36 Steel for my shafts. I chose this because I know it is an accessible material within SolidWorks, and I felt that it would be more than appropriate for the relatively low levels of torque that the gearbox transfers.
- I also decided to choose bearings before doing the full thickness calculations due to the relatively low applied loads they experience. Macmaster has fairly limited options in terms of bearings as small as what we're working with, so there was no way they would be a no-go. However, I still checked my estimates with actual calculations.

## Communicate

- One mistake I made throughout this project was mixing up the relationships between gear ratios, torque, and rotational speed. All the relationships make perfect sense if you give them a bit of thought, but rushing through calculations doesn't support critical thinking.
