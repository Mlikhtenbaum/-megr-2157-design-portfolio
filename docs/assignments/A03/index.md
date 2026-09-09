# A3 – Parametric and FEA

## Objective
Design a bar which has a circular cross-section that satisfies the provided values of the criteria given for the material, maximum deflection, and load. Determine the bar’s minimum geometry (ie.., length, diameter, and weight) through parametric design while under direct tension. Then verify the geometry through finite element analysis.

## Planning Phase:

### 1. Read and understand instructions.

I chose not to fully rewrite the instructions as I did on the last assignment because I found myself going back to the original instructions more than I was looking at my own. One initial mistake that I will document goes back long before this assignment. Back in the summer, when I downloaded SolidWorks using my UNC Charlotte email, I chose to only install the geometric functions of the program. Now I have to either install more components of the app or redownload it entirely to be able to conduct the FEA portion of the assignment. I noted this because it emphasizes the idea that putting something off always makes it more of a hassle in the future.

I also chose not to analyze previous portfolios as intensely as I did on assignment A2 because the previous iterations of A3 were based on different cross-sections.


### 2. Read necessary textbook content and take notes.

<img width="2376" height="2888" alt="A3 Textbook Notes" src="https://github.com/user-attachments/assets/2ccbcd76-8ebe-49b5-ae51-c72517035520" />
[Textbook Notes]

   
### 3. Develop understanding of parametric design workflow by watching provided content and taking notes:

These notes were taken from this [video](https://www.youtube.com/watch?v=qRBBmwv9H5o) [1]

<img width="2277" height="1528" alt="A3 Parametric Design Notes" src="https://github.com/user-attachments/assets/863b1e7e-2c45-4d1d-b4b4-c5b602a5adf4" />
[Parametric Design Video Notes]

Parametric Design Steps:
- Determine relevant parameters and use engineering equations to create relationships between them.
- Define these relationships using variables.
- Input these variables directly into a CAD model so that values automatically update when variables are altered.


### 4. Analyze and notate a YouTube video that explains the use of FEA within SolidWorks.
   
These notes were taken from this [video](https://www.youtube.com/watch?v=HQUXZJd6Fww) [2]

<img width="2434" height="1178" alt="A3 FEA Intro Notes" src="https://github.com/user-attachments/assets/a544e694-9585-4250-a9de-2760dac96f65" />
[FEA Video Notes]

ASME Citations: 
[1]Bredder, E., ed., 2020, “ Solidworks 2019 Geometric Relations & Equations,” YouTube [Online]. Available: https://www.youtube.com/watch?v=qRBBmwv9H5o. [Accessed: 08-Sep-2026]. 

[2]TforDesign, ed., 2021, “ SOLIDWORKS FEA Static Simulation in 10 Mins !,” YouTube [Online]. Available: https://www.youtube.com/watch?v=HQUXZJd6Fww. [Accessed: 08-Sep-2026]. 


## Action Phase: Parametric Modeling and FEA


### 1. Parametric CAD Design and Calculations

I chose an outer diameter of 2 inches for my beam/tube because it is an easy-to-understand size. Working with familiar sizes is advantageous to engineers because they are instantly able to determine if stress/strain values are realistic. I chose an inner diameter of 1.75 in to minimize the thickness of the tube, which, in turn, shortens the overall length of the beam. I chose 300 lbf/in^2 as my applied force value because I wanted to provide this beam (which has a fairly small outer diameter) with the greatest chance of surviving the load. I completed hand calculations to determine the resultant height, and then input the deflection equation into SolidWorks and checked my calculations using parametric formulas. The material I chose to employ within my design was 1060-H14 aluminum, which fit the criteria necessitated by the assignment's instructions.

Hand Calculations:

<img width="2521" height="1340" alt="A3 Hand Calc of L" src="https://github.com/user-attachments/assets/4e1a7a1e-e3e5-494b-9ef9-bdfc604a1b20" />

SolidWorks Parametric Calculations:

<img width="927" height="415" alt="image" src="https://github.com/user-attachments/assets/d705036a-f4a7-4d03-8ef5-4005f16a9b44" />


### Step 2: FEA SolidWorks Simulation

To create the FEA simulation within SolidWorks, I used the process described in Step 4 of the planning phase.

Von Mises Stress Map:
<img width="1920" height="1080" alt="FEA SS Von Mises Stress" src="https://github.com/user-attachments/assets/2f542c09-a227-4b09-8be9-a7a5986f5ddf" />

Deflection/Displacement Map:
<img width="1920" height="1080" alt="FEA SS Deflection " src="https://github.com/user-attachments/assets/0b587319-da55-4bb0-9182-057ab425e31e" />

The maximum stress experienced by the beam is 5.074 × 10^2 psi. I determined this number by using the "probe" feature within the stress analysis map, which automatically provides the stress at every node of the structure based on the mesh that I created. The yield strength of aluminum, as provided by the assignment description, is 40 Ksi or 40000 Psi.

Based on the formula Stress(max)=Stress(yield)/SF, the maximum resulting safety factor of my design is 78 (found by calculating 40000/507.4). That number really doesn't make a lot of sense, considering that a load of 300 lbf creates a fairly large amount of stress, especially within such a narrow beam. Therefore, I used the yield strength provided by SolidWorks to determine a more realistic safety factor. SolidWorks' provided yield strength for 1060-H14 aluminum is 1.305 x 10^4 Psi. Using this value in my calculations, I ended up with a safety factor of ~25.72, which is still high but more realistic.

<img width="1911" height="751" alt="PROBE SS Stress" src="https://github.com/user-attachments/assets/ade56ccb-af5d-448e-ba40-2ce8f484b265" />
[Stress Probe]


### Step 3: Design Reflection

a. Axial Deflection Analysis:

I assumed that this segment of A3 is referring to length rather than deflection. Deflection is given within the parameters of the assignment: "The max axial deflection of the bar is .009 inches.", and remains constant. This means that its percent error would be zero.

The axial length that I determined using hand calculation was 220.97 inches. The length determined by SolidWorks using parametric design and variable inputs was 220.95. The percent error of these two values can be found using the formula "% Error = |(SolidWorks Value - Theoretical Hand Calculated Value) / Theoretical Value| × 100%." This leads to a result of .009%, which is very accurate. The small discrepancy between these values can easily be explained by the number of decimal places used within the two calculations. This is expected due to the simple geometry of the object, which has no stress risers and a uniform cross section. I would trust both results equally, considering they are nearly identical.

b. Pin Hole Stress Concentration:

This section of A3 dictates that the pinhole calculations should be simplified into that of a hole in a flat bar in tension. This may or may not be accurate for my design, which is a tube and has significantly less cross-sectional area. Regardless, a safety factor of 25-78, depending on which yield strength is used, should leave enough room for a small pinhole.

My calculations for this step can be found within this image:
<img width="2684" height="944" alt="Pinhole Stress Riser" src="https://github.com/user-attachments/assets/0f9a77cb-f959-41df-8736-c6327e1299f2" />

A maximum stress value of 1522.2 lbf/in^2 is found by using the hole in a flat bar in tension approximation. This is still well within the safety factors of both 25 and 78, so the design is still viable (assuming, as I stated earlier, that this formula approximation is semi-valid for a tube).

### Step 4: Lesson Summary:

Throughout this assignment, I learned about different design methods and how to apply them with the SolidWorks CAD program. Global variables and parametric design are vital in cutting down the time required to create parts, and especially the time required to edit them. I also learned about the basic simulation/FEA features within SolidWorks, which are vital to the efficiency and accuracy of engineering designs. Overall, the assignment took me about 7 hours. 


## MEGR-2157 Addition

### Modify Design Parameters:

This segment of the assignment dictates that each of the variables developed within the previous iteration of the beam design must be altered. Then the final dimension and force alterations due to these changes must be estimated and determined via hand calculations. 

Original Dimensions:
- Outer Diameter: 2 inches
- Inner Diameter: 1.75 inches
- Applied Force: 300 lbf

Altered Dimensions:
- Outer Diameter: 4 inches
- Inner Diameter: 1.75 inches
- Applied Force: 400 lbf

Based on these changes, I believed that the overall length of the bar would increase due to the relationship established in the hand calculations I had conducted earlier. The increase in force will lessen this increase in length, but the length should increase regardless.

New Hand Calculations:

<img width="2291" height="1007" alt="Altered Dimension Hand Calc" src="https://github.com/user-attachments/assets/41243aaa-2f46-48df-b042-b65b9a7be044" />

My assumption that the length would increase was correct. The length increased more than ten times, going from ~221 inches to ~2290 inches. This is because the tube is experiencing such a low amount of stress relative to its cross-sectional area. For it to accumulate the deflection necessitated by the assignment instructions (.009 in), the tube must be very long.


## Decide:

One engineering decision I initially made was to use metric units. I'm a little more familiar with them, and I despise using fractional measurements. However, working in the machine shop has made me far more comfortable with U.S. Customary units since we standardize around thousandths rather than bizarre and difficult-to-comprehend fractions.

Another engineering decision I made (which is also noted in my paper notes regarding parametric design) was to use fewer sketch relations in the CAD section of this assignment than I usually do. I chose to do this to ensure that my knowledge of global variables and the assignment requirements was well conveyed. I strongly believe that having a good understanding of geometric relations is vital (and in some cases more important than global variables) to an efficient CAD workflow. 


