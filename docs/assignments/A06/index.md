# A6 – Bracket Drawing

## Objective:

Generate a comprehensive solid model and a multi-view engineering drawing that accurately represents your designed bracket, incorporating all features to ensure both strength and stiffness requirements are met.

## Step 1: Parametric Design:

### Appropriate Dimension Determination:

All of the dimensions used for this section of the assignment have been taken directly from my stress calculations on the previous project, A5. I chose to use the values gathered from stress calculations rather than those determined by deflection calculations because stress required increased dimensions in every segment. A reference multiview image from A5 is provided below to detail the part dimensions. 

<img width="2163" height="2834" alt="A5 Bracket Dimension Spec Tolerances" src="https://github.com/user-attachments/assets/e1db6c85-d6d3-44f7-93bf-19fce0a844bc" />
*The height of Feature E has been updated from .7536" to .6542" to correct a calculation error from the A5 calculations*

### Global Variable Creation:

The first step was to create a list of global variables within the Equations tab of SolidWorks. This allows me to directly import dimensions, which improves efficiency and allows for quick dimension changes if they are deemed necessary. Global variables also clean up the overall look of the file. It also allowed me to identify a dimensional issue with the height of Feature E of my bracket, which I had incorrectly calculated while completing project A5 (I had cube-rooted instead of square-rooting).

<img width="1127" height="388" alt="Gobal Equations" src="https://github.com/user-attachments/assets/84e56524-f355-4fb3-b670-94f73b92214b" />

### Upper Bracket Sketch:

The second step was sketching out the overall structure of the upper bracket and importing dimensions. I made a handful of decisions that improved efficiency during this process. I based the center of the part around the origin, which allowed me to sketch half of the part and then use the "mirror" feature to instantly create the rest. Since this is the front of the part, I sketched the feature on the front plane, which will make the final part drawing more comprehensible.

<img width="2556" height="1393" alt="Upper Bracket Sketch" src="https://github.com/user-attachments/assets/cd3cb853-4d98-45cf-a423-9189e2d2f08f" />

### Upper Bracket Extrusion:

Extruding the upper bracket sketch came next. The dimension used for this portion is the length of feature A (the strap shaft) added to the width of feature B, which connects the shaft to the rest of the bracket.

<img width="2558" height="1388" alt="Upper Bracket Extrusion" src="https://github.com/user-attachments/assets/f189f99a-81ca-4951-bfb8-6c8f9394c803" />

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

Since the bracket is designed with three different sliding fits over a rigid T-beam, model dimensions must now be adjusted, and tolerances must be established that allow these fits to function correctly. The most efficient manner of creating these relationships is as follows: Identify fit classifications that match the assignment designations, then assign appropriate dimensions and tolerances to the 3D model.

“a” intention for use where accuracy is not essential
“b” is about the closest fits that can be expected to run freely
“c” is where accurate location and minimum play is desired

Based on these guidelines and the tolerances indicated in the following diagram, we can determine the necessary fits by referencing the Machinery's Handbook:

<img width="506" height="152" alt="A5 Bracket Dimension Spec Tolerances" src="https://github.com/user-attachments/assets/26aa957c-abad-4076-8e9a-2acf07e11910" />

- Diagram of Fit "a" and the resulting bracket dimension (found on page 655 of Machinery's Handbook):

<img width="2315" height="1118" alt="Fit A" src="https://github.com/user-attachments/assets/589f5161-dcd2-4366-8dda-51cb5295069d" />

<img width="576" height="364" alt="Fit Spec for Feature A" src="https://github.com/user-attachments/assets/71b6b4f8-3103-4b2d-99fd-915b341de1f2" />


- Diagram of Fit "b" and the resulting bracket dimension (found on page 655 of Machinery's Handbook):

<img width="2368" height="1167" alt="Fit B" src="https://github.com/user-attachments/assets/5bd27b9c-a3e9-42e3-84f2-7df66a493d71" />


<img width="591" height="339" alt="Fit Spec for Feature B" src="https://github.com/user-attachments/assets/1ea734cd-4cbb-420d-b90a-d8c6f5f7e9ea" />


- Diagram of Fit "c" and the resulting bracket dimension (found on page 655 of Machinery's Handbook):

<img width="2277" height="1155" alt="Fit C" src="https://github.com/user-attachments/assets/71253433-12cf-4f14-8e61-1607298fd93f" />

<img width="376" height="379" alt="Fit Spec for Feature C" src="https://github.com/user-attachments/assets/4d343dbb-4d30-48eb-b704-237bd92eff65" />


- Final Part Drawing:

<img width="1536" height="1192" alt="Final Part Drawing" src="https://github.com/user-attachments/assets/4fc01e9d-fa64-4b2c-92f5-ebde15ed8cff" />


## Step 3: Reflections:

I actually used strength calculations to drive all of the dimensions in my parametric model. I expressed these equations in the CAD software by prompting Google Gemini to convert the same formulas I used in my hand calculations into plain text equations that I could input into SolidWorks. I chose to employ AI in this part of the design process because it was more efficient than manually typing out my formulas and painstakingly ensuring my syntax was correct. As indicated earlier within the caption for the image under the "Appropriate Dimension Determination" subheading, one of my A5 calculations was actually incorrect, and using the parametric design strategy helped me understand what was wrong and how to correct it. Luckily, since I had attributed the correct global equations to dimension the feature, it automatically updated once I corrected the equation.

One dimension in my drawing where I applied a tighter tolerance was for the segment of my bracket that contacts segment c of the rigid T-beam. Since the fit for this segment calls for "accurate location and minimum play", it must have a tighter dimensional allowance and tolerance. An LC1 fit classification dictates a maximum tolerance of +.0006" for this bracket segment, which means that the part dimension must be called out to the ten-thousandth of an inch. 

I applied a looser class to the bracket segments that are not vital in terms of fit. For example, the height of feature B (the extrusion that connects the strap shaft to the bracket body) and the shaft diameter itself are only called out to X.XX and have a tolerance of +.005/-.005. Their exact dimensions are not vital to the overall function of the part; they just need to be around their nominal size. Using looser tolerances in non-vital areas like these is an effective way to reduce manufacturing costs.

This assignment took me about 10 hours.


## Step 4: 2157 Additions: Link Part and Drawing

### Creating Global Equations:

These equations have been taken from the stress calculations completed in A5.

<img width="1126" height="242" alt="Link Global Vars" src="https://github.com/user-attachments/assets/8ca068c3-cd4d-4282-a05a-a86a2e710b52" />

### Creating Link Sketch:

The link has been created using the "slot" feature and two circles to save time.

<img width="2559" height="1392" alt="Link Sketch" src="https://github.com/user-attachments/assets/c3ca9a80-e47a-47e7-a4be-77496e5ba6c6" />

### Extruding Link Sketch:

The only thing to note about this process is that I have assumed that the cross section of the link area as it borders the 1" hole is a square. This means the width of the sketch feature at that point and the depth of the extrusion are the same.

<img width="2559" height="1389" alt="Link Extrude" src="https://github.com/user-attachments/assets/eb7e2829-7fa1-473d-a10c-0810e011db3e" />


## Decide:

One specific decision I made during this project was to alter my dimensions based on the provided T-beam tolerances only after creating my original 3D model. I didn't change them for my 3D model originally because the assignment specifically asks us to "determine the appropriate dimensions from the last assignment", and the dimensions from A5 were derived without the use of tolerances. This is why the images that outline the creation of the 3D model have slightly different dimensions than those dictated by the engineering sheet.


## Downloads:

https://drive.google.com/drive/folders/1jfPQwK0K7T63_E02jPgz66Bw1lVwktA8?usp=sharing

