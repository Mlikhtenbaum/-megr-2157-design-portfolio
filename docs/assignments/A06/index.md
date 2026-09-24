# A6 – Bracket Drawing

## Objective:

- Conduct stress analysis to determine appropriate dimensions for structural features.
- Generate free-body diagrams (FBDs) to visualize forces and constraints for each feature.
- Identify and document known and unknown variables, assumptions, and algebraic models for stress calculations.
- Perform stiffness analysis to establish minimum required dimensions based on deflection constraints.
- Compare stress and stiffness analyses to ensure structural integrity and compliance with given constraints.
- Create detailed multiview sketches illustrating dimensions derived from both stress and stiffness analyses.
- Reflect on and document key engineering lessons learned throughout the process.

## Step 1: Parametric Design:

### Appropriate Dimension Determination:

All of the dimensions used for this assignment have been taken directly from my stress calculations on the previous project, A5. I chose to use the values gathered from stress calculations rather than those determined by deflection calculations because stress required increased dimensions in every segment. A reference multiview image from A5 is provided below to detail the part dimensions. 

<img width="2628" height="3147" alt="12" src="https://github.com/user-attachments/assets/5b0cbc41-9d7c-451d-ba83-8961b9ec3615" />

### Global Variable Creation:

The first step was to create a list of global variables within the equations tab of SolidWorks. This allows me to directly import dimensions, which improves efficiency and allows for quick dimension changes if they are deemed necessary. Global variables also clean up the overall look of the file.

<img width="918" height="422" alt="Gobal Equations" src="https://github.com/user-attachments/assets/e073534e-8592-4e06-8f1d-ec28fd450fee" />

### Upper Bracket Sketch:

The second step was sketching out the overall structure of the upper bracket and importing dimensions. I made a handful of decisions that improved efficiency during this process. I based the center of the part around the origin, which allowed me to sketch half of the part and then use the "mirror" feature to instantly create the rest. Since this is the front of the part, I sketched the feature on the front plane, which will make the final part drawing more comprehensible.

<img width="1917" height="1017" alt="Upper Bracket Sketch" src="https://github.com/user-attachments/assets/5ad56713-c234-4735-aea4-68d184a38f51" />

### Upper Bracket Extrusion:

Extruding the upper bracket sketch came next. The dimension used for this portion is the length of feature A (the strap shaft) added to the width of feature B, which connects the shaft to the rest of the bracket.

<img width="1915" height="1011" alt="Upper Bracket Extrusion" src="https://github.com/user-attachments/assets/b64946e0-3d00-40b5-aaa1-7d9f90bf481c" />

### Feature B and A Conjoined Sketch:

Technically, at this point there were two features left to sketch and extrude. To aid in efficiency, I conjoined the sketches of features B and A into a single sketch. They have connected geometry, and it is therefore unnecessary to model them separately.

<img width="1917" height="1020" alt="Feature B and A Conjoined Sketch" src="https://github.com/user-attachments/assets/513b9e4d-9cc8-4d02-bd4e-9ffbe8477120" />

### Feature B Extrusion:

Moving downwards, it was time to extrude feature B. Feature A is included in this extrusion operation, but it doesn't create any issues since they extrude outwards from the same plane.

<img width="1917" height="1020" alt="Feature B Extrusion" src="https://github.com/user-attachments/assets/ed91cb63-b583-4bbd-83cb-750b117b35f0" />

### Feature A Extrusion:

Lastly, it was time to extrude feature A, the strap shaft. It has the same overall length as the width of the upper bracket, but I used separate global variables for the two in case dimension alterations are deemed necessary later on.

<img width="1917" height="1018" alt="Feature A Extrusion" src="https://github.com/user-attachments/assets/9c0e8e40-c5a0-4394-9c98-19eda72fff6b" />


## Step 2: Drawing:

Since the bracket is designed with three different sliding fits over the rigid T-beam, dimensions must be adjusted, and tolerances must be established that allow these fits to function. The most efficient manner of creating these relationships is as follows: Identify fit classifications that match the assignment designations, then assign appropriate dimensions and tolerances.

A5 Specifications:

“a” intention for use where accuracy is not essential
“b” is about the closest fits that can be expected to run freely
“c” is where accurate location and minimum play is desired

## Step 3: Reflections:


## Step 4: 2157 Additions:


## Decide


## Communicate

