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

- Calculations based on material information for ASTM A36 provided [here](https://matweb.com/search/DataSheet.aspx?MatGUID=d1844977c5c8440cb9a3a967f8909c3a)
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

#### Box: 

The gearbox box is the back section of the gearbox in which the gears are actually contained. It is made of aluminum due to the relatively low pressure exerted upon it by the tangential forces of the shafts as they undergo torsion. The steps for its creation using global variables are outlined below.

##### 1. 

Create an initial sketch, using square geometry to simplify the design. Estimate the inside width using the actual gear diameters to ensure ample clearance, and add .2" to provide at least .1" clearance on all inner faces of the box. Assume a thickness of .1" for the walls of the box.

<img width="972" height="682" alt="Gear dimension initial sketch" src="https://github.com/user-attachments/assets/7ac5bf48-bb22-4d08-9590-9759c7ad64c5" />
[Initial Gearbox Sketch Using Global Variables]

##### 2. 

Determine the necessary dimensions for the extrusions of the different box features. There were too many variables for me to consider without a sketch to reference, so I drew one on the back of my actual gearbox sketch page. Doing this allowed me to understand that the cover of my gearbox, which I will fully detail the creation of in the next section of this page, needs to be composed of two different thicknesses. Regardless, now that I understood the necessary dimensions from my sketch, I could import them into my CAD model, a process which is detailed below.

<img width="1344" height="1103" alt="Box sidewall sktch dimension" src="https://github.com/user-attachments/assets/0b8aac99-fead-4159-8f6b-b08da0688557" />
[Box Sidewall Sketch Dimension]

<img width="2479" height="1145" alt="Back Box Wall Extrusion" src="https://github.com/user-attachments/assets/53f97eee-3bed-447e-b837-8554e11c90bf" />
[Back Box Wall Extrusion]

<img width="2334" height="1143" alt="Back Box Wall Sides Extrusion" src="https://github.com/user-attachments/assets/addfc775-d0af-48bb-a600-57d267e3035d" />
[Box Side Wall Extrusion]

##### 3. 

Tap bolt holes for cover connection. M3 Bolts with a thread pitch of .5mm will be employed, as their size is appropriate for such a small design.

<img width="2004" height="1183" alt="Thread Tap SS" src="https://github.com/user-attachments/assets/72e73519-942f-4917-bf51-0092ae514afa" />
[Thread Tap for M3x.5 Bolt Using Hole Wizard]

##### 4. 

Cut out material to secure a 5/32" bearing in the back wall. A more complex sketch must be created to center components within the gearbox housing and determine the necessary position for the bearing bore.

<img width="2133" height="1188" alt="Sketch for Input Bearing Hole Definition" src="https://github.com/user-attachments/assets/492d3bac-d327-429e-a137-b56155d38cd6" />
[Sketch for Input Bearing Hole Definition]

<img width="2556" height="1184" alt="Back Bearing Bore" src="https://github.com/user-attachments/assets/11aa6a19-924d-4f46-9f01-77c3d9ba6c35" />
[Back Bearing Bore]

##### 5. 

Final Product and Global Variables

<img width="2553" height="1181" alt="Final SS" src="https://github.com/user-attachments/assets/c9d456ef-4c01-45c4-b400-e8510a710e30" />
[Final Gearbox Box]

<img width="1345" height="1143" alt="Global EQ&#39;s" src="https://github.com/user-attachments/assets/88cfecb8-8072-40ec-a2e2-5bf8e647f75d" />
[Global EQ's]


#### Cover: 

The gearbox cover is the front cover that has holes for bolts that secure it to the rest of the gearbox. It also has two toleranced holes that the brass journal bearings are pressed into. It is also made of aluminum. The steps for its creation using global variables are outlined below.

##### 1. 

Create initial sketch

<img width="938" height="980" alt="Cover Sketch sstep 1" src="https://github.com/user-attachments/assets/966ac5b0-d10d-4e4e-88a9-b1d7c6d5e609" />
[Cover Sketch]

##### 2. 

Determine the necessary y distance for the split of the thicker and thinner sections of the cover. This measurement was determined by evaluating and measuring the gearbox box model.

<img width="2259" height="1184" alt="Y distance for cover split step 2" src="https://github.com/user-attachments/assets/93686b58-8ef6-481d-a22f-223da55441a2" />
[Y Distance for Cover Split]

##### 3. 

Extrude the upper and lower sections of the cover to their respective thicknesses.

<img width="2326" height="1214" alt="Output section cover extrusion step 3a" src="https://github.com/user-attachments/assets/19b39e61-f166-410d-b6bb-a47b6f8531bb" />
[Output Section (upper) Cover Extrusion]


<img width="2360" height="1182" alt="Input section cover extrusion step 3b" src="https://github.com/user-attachments/assets/3dc84609-cf5e-4be1-9b29-d6b1937c9be3" />
[Input Section (lower) Cover Extrusion]

##### 4. 

Sketch out and cut out input and output bearing bores into the cover face. 

<img width="1180" height="1065" alt="Output Bearing Sketch Step 4a" src="https://github.com/user-attachments/assets/2c32209b-2ec0-4aaf-bffe-56fcdb8dd85b" />
[Output Bearing Sketch]

<img width="1086" height="1037" alt="Output Bearing Cut Step 4b" src="https://github.com/user-attachments/assets/3ed091a0-91fa-4ee5-b003-ac7fad57ce2b" />
[Output Bearing Cut]

<img width="1653" height="1111" alt="Input Bearing Sketch Step 4c" src="https://github.com/user-attachments/assets/9abd45c0-01a5-4020-8f16-715ae2367d29" />
[Input Bearing Sketch]

<img width="1125" height="1052" alt="Input Bearing Cut Step 4d" src="https://github.com/user-attachments/assets/2aa03b0e-c38c-40e7-8fd6-a3ae43c19aeb" />
[Input Bearing Cut]


##### 5. 

Tap holes for bolts. During this segment of the cover creation, I noticed a problem that would have occurred when I went to assemble the gearbox: the tapped holes in the gearbox box weren't deep enough to account for the thinner lower section of the cover. The bolts I am using (M3x.5x15mm) would have bottomed out. Therefore, I had to go back and increase the depth of the holes to 0.46875" instead of .25" like the top holes, to account for the thinner wall of the lower cover and the necessary gap behind the bolt. This alteration of the box design is detailed in the figure titled [Box Retapping].

<img width="1218" height="1069" alt="Tap Hole Sketch Step 5a" src="https://github.com/user-attachments/assets/62993992-2bcf-4e18-bd53-5d3a501ced3f" />
[Tap Hole Sketch]

<img width="2559" height="1184" alt="Tap Hole Wizard Step 5b" src="https://github.com/user-attachments/assets/4a9b4310-e9d1-4893-b71b-27b2ca62afc0" />
[Tap Hole Boring]

<img width="2352" height="1187" alt="Box Retapping step 5c" src="https://github.com/user-attachments/assets/8c10bc30-9339-4040-bc36-921a7910ce0c" />
[Box Retapping]

##### 6.

Final product and global equations list.

<img width="1959" height="1100" alt="Final Product step 6a" src="https://github.com/user-attachments/assets/1085fb95-e5a3-4f8d-82fc-ef9001ed6f40" />
[Final product]

<img width="2320" height="727" alt="Global EQ&#39;s step 6b" src="https://github.com/user-attachments/assets/77235691-60ce-45c9-a7e7-8e0f5b06b44e" />
[Global Equations List]


### MEGR 2157 Addition:

- Produce six multi-view CAD drawings and one assembly with complete dimensioning and proper tolerancing.
- At least two callouts for different tolerancing applied to critical features.



## Decide

- One decision I made initially was to have the longer segment of each shaft sticking out of the flanged side of its respective gear. This allows the longer shaft segment, which may experience bending forces, to resist them better.
- Another decision I made was to employ ASTM A36 Steel for my shafts. I chose this because I know it is an accessible material within SolidWorks, and I felt that it would be more than appropriate for the relatively low levels of torque that the gearbox transfers.
- I also decided to choose bearings before doing the full thickness calculations due to the relatively low applied loads they experience. Macmaster has fairly limited options in terms of bearings as small as what we're working with, so there was no way they would be a no-go. However, I still checked my estimates with actual calculations.

## Communicate

- One mistake I made throughout this project was mixing up the relationships between gear ratios, torque, and rotational speed. All the relationships make perfect sense if you give them a bit of thought, but rushing through calculations doesn't support critical thinking.
- One lesson I learned was that creating simple sketches of your design is invaluable to simplifying spatial reasoning and understanding the relationships that must be satisfied to create a function product.
