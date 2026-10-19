# A7 – FEA on Bracket and Link (2157 Addition)




## Objective:
- Use Finite Element Analysis (FEA) to improve the bracket design from previous assignments.
- Ensure high stiffness, strength, and lightweight optimization through iterative design.
- Conduct multiple FEA simulations, refining geometry based on results.
- Perform static stress analysis, including constraints, loading, and meshing selection.
- Interpret data by identifying max stress, displacement, and safety factors.
- Optimize the design by modifying geometry to enhance performance.
- Document the entire process with images, calculations, and insights.
- Reflect on key engineering lessons learned and time spent.

Use the following table to document design decisions and their quantitative results:

<img width="794" height="247" alt="Table Empty" src="https://github.com/user-attachments/assets/f347c91a-29b3-4fe8-96f6-d1d76a59d030" />

[Figure 1 - Design Table]

Your task is simply to create a high-stiffness, high-strength, and lightweight component. Use Finite Element Analysis to drive your decision-making process throughout your design. At each step of the analysis, and before you make geometric changes, make sure the component’s results (stress/displacement/Safety Factor) converge to within a 7% difference. Achieve this by modifying the number of elements. If, after three attempts to converge use the stiffness and stress from the finer mesh size, use the finest mesh size and proceed through the process.

### Proposed workflow: Bracket

Step 1: Take the initial design (design 1) and run coarse>med>fine FEA. Find where stress acts maximally and minimally and add/remove material respectively to optimize structure strength and weight. 
Step 2: Take the new design from Step 1 (design 2) and run coarse>med>fine FEA. Identify where stress is maximal and minimal, and add/remove material accordingly to optimize structure strength and weight. 
Step 3: Take the new design from Step 2 (design 3) and run coarse>med>fine FEA. Identify where stress is maximal and minimal, and add/remove material accordingly to optimize structure strength and weight. 

Note: Use the following difference formula for stress/displacement/safety-factor to determine if fine mesh FEA is necessary or if coarse and medium FEAs are adequate. Only run a fine mesh FEA if the (% difference between coarse and medium FEA) > 7%.

<img width="239" height="151" alt="Difference Formula" src="https://github.com/user-attachments/assets/c3dcb894-626f-4812-a556-77c058b0aa05" />

[Figure 2 - Difference Formula]


### Proposed workflow: Link (2157 Addition)

The workflow for the link follows the same structure as that of the bracket, since they experience the same applied force.




## Analyze and Optimize: Bracket:



### Step 1: Overall FEA Setup

##### 1: Fixturing:

<img width="2250" height="1376" alt="Initial Design Fixturing" src="https://github.com/user-attachments/assets/c490f6f2-fde0-4073-93d4-4c506e661e17" />

[Figure 3 - fixed fixture]

##### 2: Split Creation for Force Application

<img width="2222" height="1375" alt="Split Creation for Force Application" src="https://github.com/user-attachments/assets/d04e70c3-ab7e-4c58-a8d8-76a2d99d6228" />

[Figure 4 - Split Creation]

##### 3: Force Application (1200lbf):

<img width="2173" height="1380" alt="External Load Application" src="https://github.com/user-attachments/assets/8b007c4b-ce93-425a-ac16-a3b638b87315" />

[Figure 5 - Force Application Design 1]

* For all following FEAs within the "## Analyze and Optimize: Bracket:" heading, specific force application and fixturing screenshots will not be provided, as they are ubiquitous in terms of position for each mesh iteration.*
  


### Step 2: Design 1 FEA:

There are no additions or alterations to consider in the first step of the part optimization. FEA must be conducted first to determine where stress and displacement maxima occur, and then optimization can occur.

##### 1. Coarse Mesh FEA:

<img width="2204" height="1380" alt="Coarse Mesh Setup" src="https://github.com/user-attachments/assets/269df0de-76d5-48e7-9970-7fa5c446f5d6" />

[Figure 6 - Coarse Mesh Creation]

<img width="2550" height="1384" alt="Coarse Mesh FEA Stress (2)" src="https://github.com/user-attachments/assets/52d06dc6-388e-4579-a51d-60d3dc9fc806" />

[Figure 7 - Coarse Mesh FEA Stress]

<img width="2550" height="1388" alt="Coarse Mesh FEA Displacement" src="https://github.com/user-attachments/assets/1e39ab0b-c357-41bf-bd78-c8401d2f3c48" />

[Figure 8 - Coarse Mesh FEA Displacement]

<img width="2554" height="1391" alt="Coarse Mesh FEA SF" src="https://github.com/user-attachments/assets/46dba5ad-c8e9-4e9a-91d7-b94cdc4fd23e" />

[Figure 9 - Coarse Mesh FEA SF]

##### 2. Medium Mesh FEA:

<img width="2550" height="1382" alt="Med Mesh Creation" src="https://github.com/user-attachments/assets/55ae3d5e-ac5f-444d-ae7f-658dc9c64de7" />

[Figure 10 - Medium Mesh Creation]

<img width="2558" height="1386" alt="Med FEA Stress" src="https://github.com/user-attachments/assets/d8bba55c-8d84-4174-a8a2-7e873570bdcd" />

[Figure 11 - Medium Mesh FEA Stress]

<img width="2559" height="1383" alt="Med FEA Disp" src="https://github.com/user-attachments/assets/affe0a20-33fa-4d6a-9864-3ddcc3260682" />

[Figure 12 - Medium Mesh FEA Displacement]

<img width="2559" height="1384" alt="Med FEA SF" src="https://github.com/user-attachments/assets/68c9836c-c574-458a-b61e-acab5f3b6d10" />

[Figure 13 - Medium Mesh FEA SF]

##### 3. Fine Mesh FEA: 
- Fine Mesh FEA is required due to the difference in coarse mesh vs. medium mesh stress being larger than 7%:
Percent Difference = |(New Value - Previous Value) / Previous Value| * 100%
Percent Difference = |(140,100 - 155,700) / 155,700| * 100%
Percent Difference = |-15,600 / 155,700| * 100%
Percent Difference = 0.100192 * 100% = 10.02%

<img width="2559" height="1384" alt="Fine Mesh Creation" src="https://github.com/user-attachments/assets/f2baf1c4-5954-44ab-9be6-f1b85fc73a6d" />

[Figure 14 - Fine Mesh Creation]

<img width="2558" height="1385" alt="Fine Mesh FEA Stress" src="https://github.com/user-attachments/assets/5c6d85b5-ee04-46bd-96b5-c467807250d0" />

[Figure 15 - Fine Mesh FEA Stress]

<img width="2556" height="1382" alt="Fine Mesh FEA Disp" src="https://github.com/user-attachments/assets/cbcfc486-ad06-44d3-9110-abb34feabff8" />

[Figure 16 - Fine Mesh FEA Displacement]

<img width="2559" height="1390" alt="Fine Mesh FEA SF" src="https://github.com/user-attachments/assets/6ecd7662-e0b6-4e4d-82e9-8b11cb740502" />

[Figure 17 - Fine Mesh FEA SF]



### Step 2: Design 2 FEA and alterations


#### 1. Design Alterations:

After analyzing the results from the three previous FEAs, multiple design considerations became apparent:

1. The flange that connects the upper portion of the bracket to the strap shaft is significantly under-engineered, since I modelled it as an axially loaded bar, rather than one being acted upon by a bending stress. Material must be added to help support the structure and resist the bending force applied by the strap. To amend this issue, I will model a rib on the rear end of the shaft that will help resist bending, and a fillet to add material to the flange (also to resist bending). The rib width will be 1/2 of the strap shaft diameter, and it will be 1/4 as thick as the length of the shaft. The fillets employed on the rib feature and flange are .1".

2. The upper portion of the bracket experiences very little stress, which means a good portion of the material can be removed (as long as the previously mentioned design alteration does not redistribute the force in a manner that compromises the upper bracket. I will use a fillet to smooth out and remove material from this segment of the bracket, which will reduce its overall weight. Fillets are an important consideration in such a design for another reason as well - they dull the corners of the design, making it safer to use and negating the risk of it snagging and possibly tearing the strap that it supports. The fillets employed on the upper bracket feature are .25" to remove more material.

<img width="2554" height="1381" alt="Design 2 Rib Sketch (half shaft d)" src="https://github.com/user-attachments/assets/16b48d48-6c67-40ef-9b6b-ffb5dd9b4c5d" />

[Figure 18 - Design 2 Rib Sketch]

<img width="2559" height="1382" alt="Design 2 Rib Extrusion (qtr bracket thickness)" src="https://github.com/user-attachments/assets/8b6f9bef-195c-43ed-975f-7b9668fc79bf" />

[Figure 19 - Design 2 Rib Extrusion]

<img width="2555" height="1394" alt="Rib Fillet" src="https://github.com/user-attachments/assets/d123ebc1-03d3-41fc-a5f2-3878064cd05c" />

[Figure 20 - Design 2 Rib Fillet 1]

<img width="2556" height="1385" alt="Rib Fillet 2" src="https://github.com/user-attachments/assets/2da86550-e579-4069-a605-b68f766f5943" />

[Figure 21 - Design 2 Rib Fillet 2]

<img width="2559" height="1381" alt="Upper Bracket Fillet  25in" src="https://github.com/user-attachments/assets/9d9df6d9-7185-4cb3-a501-0ac81265e02b" />

[Figure 22 - Design 2 Upper Bracket Fillet]


#### 2. Design 2 FEA:

##### 1. Coarse Mesh FEA:

<img width="2559" height="1385" alt="Coarse Mesh Creation" src="https://github.com/user-attachments/assets/7beb6394-edd8-4136-875c-6923ec426dce" />

[Figure 23 - Coarse Mesh Creation]

<img width="2559" height="1382" alt="Coarse Mesh FEA Stress" src="https://github.com/user-attachments/assets/1bd80a19-9c64-465b-b414-b99cf69ccef2" />

[Figure 24 - Coarse Mesh FEA Stress]

<img width="2559" height="1385" alt="Coarse Mesh FEA Defl" src="https://github.com/user-attachments/assets/621695bd-7c80-4eee-b8e4-2cf78dc126e9" />

[Figure 25 - Coarse Mesh FEA Deflection]

<img width="2554" height="1382" alt="Coarse Mesh FEA SF" src="https://github.com/user-attachments/assets/957cb283-0ea0-4d6a-bf9a-d98279eef2cf" />

[Figure 26 - Coarse Mesh FEA SF]

##### 2. Medium Mesh FEA:

<img width="2559" height="1386" alt="Med Mesh Creation" src="https://github.com/user-attachments/assets/17687eb9-ace7-46d2-808c-2be3bd227b2f" />

[Figure 27 - Medium Mesh Creation]

<img width="2559" height="1384" alt="Med Mesh FEA Stress" src="https://github.com/user-attachments/assets/8d4cd85d-f0e8-454f-9249-db8e0bd502ac" />

[Figure 28 - Medium Mesh FEA Stress]

<img width="2559" height="1384" alt="Med Mesh FEA Defl" src="https://github.com/user-attachments/assets/3203506e-f0c1-4b31-a235-6b8bdbd6facd" />

[Figure 29 - Medium Mesh FEA Deflection]

<img width="2559" height="1379" alt="Med Mesh FEA SF" src="https://github.com/user-attachments/assets/23c89028-362a-44ca-804b-60d6e640cfc0" />

[Figure 30 - Medium Mesh FEA SF]

##### 3. Fine Mesh FEA: 

Fine Mesh FEA is not required due to the difference in coarse mesh vs. medium mesh stress being less than 7%:
Percent Difference = |(New Value - Previous Value) / Previous Value| * 100%
Percent Difference = |(63,140 - 61,530) / 61,530| * 100%
Percent Difference = |1,610 / 61,530| * 100%
Percent Difference = 0.026166 * 100% = 2.62%



### Step 3: Design 3 FEA and alterations


#### 1. Design Alterations:

After analyzing the results from the three previous FEAs, multiple design considerations became apparent:

1. The stress riser created by the sudden geometric transition from the shaft to the bracket flange was too extreme to be sustained by simply adding a rib, as I had done in the previous design iteration. More drastic measures must be taken to improve the design and more effectively distribute stress. To alleviate the stress concentration within this segment of the part, I chose to add a secondary flange on the other side of the shaft and add fillets to the transition areas between the shaft and both flanges (the old and new ones). These are valid design improvements because the strap can easily be threaded into the gap between the two flanges, and since the strap is relatively malleable, it can flex to accommodate the fillet radii. The flange thickness will be 1/4 the length of the shaft, and .1" fillets will be used to better transition it into the rest of the flange. .06" fillets will be used to alleviate the stress risers that develop at the connection between the flanges and the shaft, to not cause overt deflection of the strap.

2. To help reduce the weight created by the addition of another flange, material will be removed by adding a realistic amount of material removal fillets to the outside of the bracket. It is important to not just throw them everywhere, as that would make manufacturing the bracket even more difficult. As is, it would likely already have to be composed of multiple components, or created using investment casting and then machined down to the correct tolerances.

3. *Addendum, see Figure #35*: The applied force within the FEA simulation must be redefined to account for the fillets added between the shaft and flanges.

<img width="2559" height="1381" alt="Flange 2 Sketch" src="https://github.com/user-attachments/assets/940ed709-7275-4d48-bad0-8cd6a0033796" />

[Figure 31 - Flange 2 Sketch]

<img width="2559" height="1384" alt="Flange 2 Extrusion" src="https://github.com/user-attachments/assets/dda82287-2be0-48c2-a22c-ad80feb75241" />

[Figure 32 - Flange 2 Extrusion]

<img width="2493" height="1381" alt="Flange 2 Bracket Fillet" src="https://github.com/user-attachments/assets/5300c335-780a-46bf-b5bb-185a9a3cc018" />

[Figure 33 - Flange 2 Bracket Fillet]

<img width="2559" height="1380" alt="FlangeShaft Fillet" src="https://github.com/user-attachments/assets/dd161e55-b700-45d9-a1b7-8d0eea9d141e" />

[Figure 34 - Shaft/Flange Fillet]

<img width="2538" height="1382" alt="Force Redef" src="https://github.com/user-attachments/assets/fd60ec27-2962-4093-b079-1cf20ed01cf6" />

[Figure 35 - Redefinition of Applied Force]


#### 2. Design 3 FEA:

##### 1. Coarse Mesh FEA:

<img width="2559" height="1379" alt="Coarse Mesh" src="https://github.com/user-attachments/assets/12e853f4-658d-40b1-a3ad-2653076a0fdc" />

[Figure 36 - Coarse Mesh Creation]

<img width="2557" height="1382" alt="Coarse FEA Stress" src="https://github.com/user-attachments/assets/815ee50b-b1f1-4ea9-a6f9-2dc6cbbc5212" />

[Figure 37 - Coarse Mesh FEA Stress]

<img width="2543" height="1379" alt="Coarse FEA Displacement" src="https://github.com/user-attachments/assets/236d7c14-4e7c-4d38-9303-0fb49cd9d44b" />

[Figure 38 - Coarse Mesh FEA Displacement]

<img width="2559" height="1383" alt="Coarse Mesh SF" src="https://github.com/user-attachments/assets/6fab6370-ac43-43be-8908-2788b461f73d" />

[Figure 39 - Coarse Mesh FEA SF]

##### 2. Medium Mesh FEA:

<img width="2557" height="1384" alt="Med Mesh" src="https://github.com/user-attachments/assets/11369e26-da0b-424d-8f82-fe2f365d6f71" />

[Figure 40 - Medium Mesh Creation]

<img width="2549" height="1379" alt="Med FEA Stress" src="https://github.com/user-attachments/assets/a1286b58-5f0e-437f-a1c8-b3904ac12482" />

[Figure 41 - Medium Mesh FEA Stress]

<img width="2559" height="1386" alt="MED FEA Displacement" src="https://github.com/user-attachments/assets/7b2bc1e2-0a75-4ad3-acf8-27f156af8cfc" />

[Figure 42 - Medium Mesh FEA Displacement]

<img width="2559" height="1385" alt="Med FEA SF" src="https://github.com/user-attachments/assets/5f3f6fda-6da3-40bd-a9e5-b561923f610a" />

[Figure 43 - Medium Mesh FEA SF]

##### 3. Fine Mesh FEA: 

Fine Mesh FEA is not required due to the difference in coarse mesh vs. medium mesh stress being less than 7%:
Percent Difference = |(New Value - Previous Value) / Previous Value| * 100%
Percent Difference = |(57,660 - 56,590) / 56,590| * 100%
Percent Difference = |1,070 / 56,590| * 100%
Percent Difference = 0.018908 * 100% = 1.89%



### Step 4: Final Design Iteration Table and Lessons Learned


#### 1. Design Table:

<img width="1082" height="788" alt="Table Done" src="https://github.com/user-attachments/assets/d8060bc2-dc2a-49f7-8a5b-722d966735f0" />

[Figure 44 - Populated Design Table]


#### 2. Lessons Learned:

A few of the major lessons I learned from this project were as follows:
1. I learned about the importance of eliminating stress risers within a design, as they can create unforeseen failures in a part that should otherwise be able to withstand an applied load.
2. I learned about the importance of correctly identifying modes of failure within different segments of a design, as misidentifying the effects of applied loads can be disastrous.

Overall, if I were to continue creating design iterations for this bracket, I would thicken the upper walls of the design to reduce deflection and better distribute stress. I would also redesign the shaft connection, making it symmetrical so that it would not deflect unevenly.




## Analyze and Optimize: Link (2157 Addition)


#### Step 1: Overall FEA Setup:

Both applied force and fixturing require split lines to accurately simulate what will occur when the link is loaded.

<img width="2254" height="1380" alt="Fixturing" src="https://github.com/user-attachments/assets/a46abd74-f3f3-48be-b242-48d2683dfa5c" />

[Figure 45 - Link Fixturing]

<img width="2550" height="1380" alt="Force Application" src="https://github.com/user-attachments/assets/1ad36114-708a-4cab-8fbe-d2fdc2f22f7b" />

[Figure 46 - Link Force Application]


#### 2. Design 1 FEA:

##### 1. Coarse Mesh FEA

<img width="2559" height="1385" alt="Coarse Mesh Creation" src="https://github.com/user-attachments/assets/eabc713a-c54b-4e88-8ab8-773b7934025c" />

[Figure 47 - Coarse Mesh Creation]

<img width="2559" height="1383" alt="Coarse FEA Stress" src="https://github.com/user-attachments/assets/22ebe087-7ba0-4581-a8f9-d8c29f1582b8" />

[Figure 48 - Coarse Mesh FEA Stress]

<img width="2559" height="1386" alt="Coarse FEA Defl" src="https://github.com/user-attachments/assets/a6f44de3-e02d-4023-b680-ac1438ebdccd" />

[Figure 49 - Coarse Mesh FEA Deflection]

<img width="2559" height="1383" alt="Coarse FEA SF" src="https://github.com/user-attachments/assets/b0b1a5ea-351e-4636-999f-336f47b78cac" />

[Figure 50 - Coarse Mesh FEA SF]

##### 2. Medium Mesh FEA

<img width="2323" height="1378" alt="MED MESH" src="https://github.com/user-attachments/assets/7eba0617-1d0b-445c-ad1e-0e1dc99e5a8a" />


<img width="2559" height="1380" alt="MED FEA Stress" src="https://github.com/user-attachments/assets/d3265229-9074-4841-a255-f7713869ba17" />


<img width="2559" height="1381" alt="MED FEA Defl" src="https://github.com/user-attachments/assets/64b375b4-4f87-4cc1-a3fd-ee6ca57caf6d" />


<img width="2539" height="1365" alt="MED FEA SF" src="https://github.com/user-attachments/assets/16e2691d-967b-4efc-8007-e5fac4e4f6e8" />






#### 2. Design 2 FEA:

##### 1. Coarse Mesh FEA

##### 2. Medium Mesh FEA


#### 2. Design 3 FEA:

##### 1. Coarse Mesh FEA

##### 2. Medium Mesh FEA










## Decide:

One specific engineering decision I initially (incorrectly) made was to apply a rolling/sliding fixture to my bracket rather than a fixed one. I went with this choice since it is technically a more accurate representation of how the bracket is actually held in place on its mount. However, this fixturing method is invalid since the bracket is not part of a constrained assembly and will simply float off into space if it is not fixed.

Another theoretical mistake in my design process was caused by my creation of a secondary flange on the bracket. The 2157 addition of a link will no longer fit unless the bracket is assembled using multiple components. The height of both flanges would also have to be increased to allow the link to fit correctly.


## Communicate:

Part Files for each design and FEA analysis can be found here[]

