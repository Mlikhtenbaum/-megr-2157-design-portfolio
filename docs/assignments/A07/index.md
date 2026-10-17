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

## Analyze and Optimize: Bracket

### Step 1: Initial Design FEA

There are no additions or alterations to consider in the first step of the part optimization. FEA must be conducted first to determine where stress and displacement maxima occur, and then optimization can occur.


### Step 2: Design 2 FEA and alterations

### Step 3: Design 3 FEA and alterations

## Analyze and Optimize: Link (2157 Addition)



## Decide


## Communicate
Part Files for each design and FEA analysis can be found here[]

