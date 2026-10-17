# A7 – FEA on Bracket and Link (2157 Addition)

## Objective
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

##### 4: Split Creation for Force Application

<img width="2222" height="1375" alt="Split Creation for Force Application" src="https://github.com/user-attachments/assets/d04e70c3-ab7e-4c58-a8d8-76a2d99d6228" />

[Figure 4 - Split Creation]

##### 3: Force Application (1200lbf):

<img width="2173" height="1380" alt="External Load Application" src="https://github.com/user-attachments/assets/8b007c4b-ce93-425a-ac16-a3b638b87315" />

[Figure 5 - Force Application Design 1]

* For all following FEAs within the "## Analyze and Optimize: Bracket:" heading, specific force application and fixturing screenshots will not be provided, as they are ubiquitous in terms of position for each mesh iteration.*
  

### Step 1: Initial Design FEA:

There are no additions or alterations to consider in the first step of the part optimization. FEA must be conducted first to determine where stress and displacement maxima occur, and then optimization can occur.

#### 1. Coarse Mesh FEA:

<img width="2204" height="1380" alt="Coarse Mesh Setup" src="https://github.com/user-attachments/assets/269df0de-76d5-48e7-9970-7fa5c446f5d6" />

[Figure 6 - Coarse Mesh Creation]

<img width="2550" height="1384" alt="Coarse Mesh FEA Stress (2)" src="https://github.com/user-attachments/assets/52d06dc6-388e-4579-a51d-60d3dc9fc806" />

[Figure 7 - Coarse Mesh FEA Stress]

<img width="2550" height="1388" alt="Coarse Mesh FEA Displacement" src="https://github.com/user-attachments/assets/1e39ab0b-c357-41bf-bd78-c8401d2f3c48" />

[Figure 8 - Coarse Mesh FEA Displacement]

<img width="2554" height="1391" alt="Coarse Mesh FEA SF" src="https://github.com/user-attachments/assets/46dba5ad-c8e9-4e9a-91d7-b94cdc4fd23e" />

[Figure 9 - Coarse Mesh FEA SF]

#### 2. Medium Mesh FEA:

<img width="2550" height="1382" alt="Med Mesh Creation" src="https://github.com/user-attachments/assets/55ae3d5e-ac5f-444d-ae7f-658dc9c64de7" />

[Figure 10 - Medium Mesh Creation]

<img width="2558" height="1386" alt="Med FEA Stress" src="https://github.com/user-attachments/assets/d8bba55c-8d84-4174-a8a2-7e873570bdcd" />

[Figure 11 - Medium Mesh FEA Stress]

<img width="2559" height="1383" alt="Med FEA Disp" src="https://github.com/user-attachments/assets/affe0a20-33fa-4d6a-9864-3ddcc3260682" />

[Figure 12 - Medium Mesh FEA Displacement]

<img width="2559" height="1384" alt="Med FEA SF" src="https://github.com/user-attachments/assets/68c9836c-c574-458a-b61e-acab5f3b6d10" />

[Figure 13 - Medium Mesh FEA SF]

#### 3. Fine Mesh FEA: 
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


### Step 3: Design 3 FEA and alterations



## Analyze and Optimize: Link (2157 Addition)


## Decide
One specific engineering decision I initially made was to apply a rolling/sliding fixture to my bracket rather than a fixed one. I went with this choice since it is technically a more accurate representation of how the bracket is actually held in place on its mount. However, this fixturing method is invalid since the bracket is not part of a constrained assembly and will simply float off into space if it is not fixed.

## Communicate
Part Files for each design and FEA analysis can be found here[]

