# A3 – Parametric and FEA

## Objective
Design a bar which has a circular cross-section that satisfies the provided values of the criteria given for the material, maximum deflection, and load. Determine the bar’s minimum geometry (ie.., length, diameter, and weight) through parametric design while under direct tension. Then verify the geometry through finite element analysis.

## Planning Phase:

###1. Read and understand instructions.

I will not be fully rewriting the instructions as I did on the last assignment because I found myself going back to the original instructions more than I was looking at my own. One initial mistake that I will document goes back long before this assignment. Back in the summer, when I downloaded SolidWorks using my Charlotte email, I chose to only install the geometric functions of the program. Now I have to either install more components of the app or redownload it entirely to be able to conduct the FEA portion of the assignment. I noted this because it emphasizes the idea that putting something off always makes it more of a hassle in the future.

I also chose not to analyze previous portfolios as intensely as I did on assignment A2 because the previous iterations of A3 were based on different cross-sections.


###2. Read necessary textbook content and take notes.

<img width="2376" height="2888" alt="A3 Textbook Notes" src="https://github.com/user-attachments/assets/2ccbcd76-8ebe-49b5-ae51-c72517035520" />
[Textbook Notes]

   
###3. Develop understanding of parametric design workflow by watching provided content and taking notes:

These notes were taken from this [video](https://www.youtube.com/watch?v=qRBBmwv9H5o) [1]

<img width="2277" height="1528" alt="A3 Parametric Design Notes" src="https://github.com/user-attachments/assets/863b1e7e-2c45-4d1d-b4b4-c5b602a5adf4" />
[Parametric Design Video Notes]

Parametric Design Steps:
- Determine relevant parameters and use engineering equations to create relationships between them.
- Define these relationships using variables.
- Input these variables directly into a CAD model so that values automatically update when variables are altered.


###4. Analyze and notate a YouTube video that explains the use of FEA within SolidWorks.
   
These notes were taken from this [video](https://www.youtube.com/watch?v=HQUXZJd6Fww) [2]

<img width="2434" height="1178" alt="A3 FEA Intro Notes" src="https://github.com/user-attachments/assets/a544e694-9585-4250-a9de-2760dac96f65" />
[FEA Video Notes]

ASME Citations: 
[1]Bredder, E., ed., 2020, “ Solidworks 2019 Geometric Relations & Equations,” YouTube [Online]. Available: https://www.youtube.com/watch?v=qRBBmwv9H5o. [Accessed: 08-Sep-2026]. 

[2]TforDesign, ed., 2021, “ SOLIDWORKS FEA Static Simulation in 10 Mins !,” YouTube [Online]. Available: https://www.youtube.com/watch?v=HQUXZJd6Fww. [Accessed: 08-Sep-2026]. 


## Action Phase: Parametric Modeling and FEA


###1. Parametric CAD Design and Calculations

I chose an outer diameter of 2 inches for my beam/tube because it is an easy-to-understand size. Working with familiar sizes is advantageous to engineers because they are instantly able to determine if stress/strain values are realistic. I also chose an inner diameter of 1.75 in to minimize the thickness of the tube, which, in turn, shortens the overall length of the beam. I chose 300 lbf/in^2 as my applied force value because I wanted to give this original, fairly small dimension of D = 2 in the greatest chance of surviving the load. I completed hand calculations to determine the resultant height, and then input the equation into SolidWorks and checked my calculations using parametric formulas. The material I chose to employ within my design was 1060-H14 aluminum, which fit the criteria necessitated by the assignment's instructions.

Hand Calculations:

<img width="2521" height="1340" alt="A3 Hand Calc of L" src="https://github.com/user-attachments/assets/4e1a7a1e-e3e5-494b-9ef9-bdfc604a1b20" />

SolidWorks Parametric Calculations:

<img width="927" height="415" alt="image" src="https://github.com/user-attachments/assets/d705036a-f4a7-4d03-8ef5-4005f16a9b44" />


###Step 2: FEA SolidWorks Simulation

To create the FEA simulation within SolidWorks, I used the process described in Step 4 of the planning phase.

Von Mises Stress Map:
<img width="1920" height="1080" alt="FEA SS Von Mises Stress" src="https://github.com/user-attachments/assets/2f542c09-a227-4b09-8be9-a7a5986f5ddf" />

Deflection/Displacement Map:
<img width="1920" height="1080" alt="FEA SS Deflection " src="https://github.com/user-attachments/assets/0b587319-da55-4bb0-9182-057ab425e31e" />

The maximum stress experienced by the beam is 5.074 × 10^2 psi. I determined this number by using the "probe" feature within the stress analysis map, which automatically provides the stress at every node of the structure based on the mesh that I created. The yield strength of aluminum, as provided by the assignment description, is 40 Ksi or 40000 Psi.

Based on the formula Stress(max)=Stress(yield)/SF, the maximum resulting safety factor of my design is 78 (found by calculating 40000/507.4). That number really doesn't make a lot of sense, considering that a load of 300 lbf creates a fairly large amount of stress, especially within such a narrow beam. Therefore, I am going to use the yield strength provided by SolidWorks to determine a more realistic safety factor. SolidWorks' provided yield strength for 1060-H14 aluminum is 1.305 x 10^4 Psi. Using this value in my calculations, I end up with a safety factor of ~25.72, which is still high but more realistic.

<img width="1911" height="751" alt="PROBE SS Stress" src="https://github.com/user-attachments/assets/ade56ccb-af5d-448e-ba40-2ce8f484b265" />
[Stress Probe]

###Step 3: Design Reflection

The axial deflection that I found using hand calculations was 220.97 inches.

## Analyze:


## Decide:

One engineering decision I initially made was to use metric units. I'm a little more familiar with them, and I despise using fractional measurements. However, working in the machine shop has made me far more comfortable with U.S. Customary units since we standardize around thousandths rather than bizarre and difficult-to-comprehend fractions.

Another engineering decision I made (which is also noted in my paper notes regarding parametric design) was to use fewer sketch relations in the CAD section of this assignment than I usually do. I chose to do this to ensure that my knowledge of global variables and the assignment requirements was well conveyed. I strongly believe that having a good understanding of geometric relations is vital (and in some cases more important than global variables) to an efficient CAD workflow. 

## Communicate:

