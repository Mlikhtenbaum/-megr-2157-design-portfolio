# A2 – Truss Stress Analysis

## Objective
Design a truss and document your process.

## Initial Planning

Phase 1: Reading and Understanding: 0:10

 Reading and understanding the assignment in its entirety is vital to creating an effective engineering solution. On 9/1/26, from 11:05 to 11:15, I dedicated my time to ensuring I was familiar with the general process behind each step of the truss design process.

Phase 2: Plan Summarization and Restructuring: 1:00

 My next step was to summarize the assignment's main points and subpoints and create a plan and timeline/process on paper. I also wanted to restructure some of the points to make more sense chronologically. I chose to do this stage of the design on paper because it allowed me to structure wording and graphics in a way that best aided my visualization of the project. This stage ranged from 11:17 to 12:15 on 9/1/26. 
 
 Writing out the details in this manner elucidated a few factors for me. Firstly, I realized that solving symbolically means writing out the equations using variables. Had I not read and rewritten this step, I would have assumed it meant to explain my process using words. Simple misunderstandings like these can be costly, both to an assignment grade and an engineering project, so minimizing them is vital. Secondly, I realized how important having legible handwriting and proper grammar is as an engineer. If you are creating project plans and sharing them with others, your plans must be comprehensible. Thirdly, I recognized an important method that could have allowed me to increase efficiency. Rather than listing each step of my intended process in paragraph form, I should have listed each subpoint as a line within a list. That way, I could have checked off each feature as I went. I also realized that labelling each junction and member of the truss would be beneficial for the final stage of my process. This would be the additional requirement dictated by the 2157 section - identifying predicted failure modes within each member. If each truss rod is labelled, it will be much easier to interpret the final calculations.

Here is my restructured plan:
<img width="2414" height="3074" alt="1" src="https://github.com/user-attachments/assets/4f1b0ab3-8992-4dec-8ec2-54c73b15cac1" />
<img width="2212" height="2850" alt="2" src="https://github.com/user-attachments/assets/ea8bacef-ba52-4cd3-a1ec-8e0a41247db8" />

Phase 3: Portfolio Analysis: 0:37

  Throughout this phase of my engineering process, I analyzed previous designs that have been submitted by students. This would allow me to have a better overview of how the end result should look, which may even alter how I want to conduct my process.

 The first portfolio I looked through for this stage of the process was Luke DeVries' (which can be found at this [link](https://instructure.charlotte.edu/eportfolios/4880/welcome)). I found Luke's portfolio very helpful in providing an overview of an effective structure and documentation process. The structure of his portfolio perfectly lines up with the steps of the assignment, which made it very easy to navigate. His documentation is replete, especially in describing the mistakes that he encountered throughout his design process (which is very admirable). I planned on using the information I gained from his portfolio to ensure that I completed all my calculations correctly initially, rather than having to go back and redo them. His perseverance in creating two separate truss designs was also insightful, as it inspired me to read more about truss design and how symmetry can be beneficial.

 The second portfolio I read was Sammari Tate's (which can be accessed at https://uncc.instructure.com/eportfolios/4900/home/landing-page). Sammari's portfolio was very detailed and organized, which I hoped to achieve in my portfolio as well. One detail that I appreciated within Sammari's project was a simple yet uncommon measure in daily life: differentiating between mass and weight. I would have realized the necessity for further calculation eventually, but Sammari saved me the trouble of face-palming once I remembered to use newtons rather than kilograms. I appreciate maintaining an efficient work process, and overlooking small but vital details like these due to everyday simplifications can mean spending more time than necessary on a project. Proper calculations and vocabulary, combined with an efficient workflow, are essential to engineering success.

Phase 4: Truss Research: 0:41

 For this phase of the planning process, I planned to read an engineering article about basic truss design to gain a general understanding of the do's and don'ts. The truss article I chose to analyze was part of the Engineering Statics: Open and Interactive textbook; the link for which is: https://engineeringstatics.org/Chapter_06-trusses.html. While reading this segment of the textbook, I learned and refreshed my memory regarding various aspects of static truss design. I learned about the importance of zero-force members and why engineers implement them within trusses. They are vital to supporting other members at load-intensive joints and resisting buckling forces [1]. Although we are not considering buckling within this assignment, it is still an important concept to understand. Secondly, I refreshed my memory regarding the identification of zero-force members, which will help me design a redundant yet efficient truss design.

ASME Textbook Citation: 
[1]Baker, D. W., and Haynes, W., 2021, Engineering Statics: Open and Interactive, Daniel Baker and William Haynes. 

This part of the planning phase ranged from 7:40 pm to 8:21 pm. I also went back and edited the previous planning segments to use past-tense terminology during this period.

## Truss Design

## Step 1:

Initial Design:

 The first step I completed within my truss design process was sketching out Figure 1 and creating two different truss designs based on the given dimensions. While sketching out these trusses, my design process was fairly arbitrary, but there was one dictating element in the mix. I wanted to involve as many triangles as I could. This is because I know they are the most supportive shape when designing structures that encounter loads from multiple directions. After creating my two designs, I sat down and began to analyze them mentally, both visually and mathematically, eliminating zero-force members in my basic calculations and ensuring that my designs were realistic. After considering their viability, design B was the clear winner, based on two advantages. It has no zero-force members, which are important in real-world applications but are irrelevant to our controlled situation. This lack of zero-force members allows the design to be lighter than a truss with more beams/rods. The second superiority of design B theoretically offsets this aforementioned disadvantage. It should - and I hadn't conducted the calculations yet - still be able to handle the applied loads even if one of the members were to fail. Of course, this distinction depends on the cross-sectional area of the rods that make up the truss, and the material it's made from. However, in theory, design B is the winner under both of these considerations.

Here are my initial design sketches:

<img width="2663" height="3410" alt="3 (Truss Design)" src="https://github.com/user-attachments/assets/6e212439-af8a-46ed-95eb-f895b05d4fae" />

Length and external force equilibrium: 1:40

<img width="2541" height="3340" alt="Length and External Forces" src="https://github.com/user-attachments/assets/606bca56-4612-42c8-ab59-4ccb34d8c3a2" />

 Continuing this process, I redrew Design B more accurately and inputted the given measurements into my diagram. It was time to get into determining lengths and forces. One important lesson I learned throughout this process is that it is important to identify determinate joints prior to beginning the solving process. I drew joint E prior to solving joint C, which was inefficient since I needed info from C's solution to determine the forces on E. At least, that's what I thought. In reality, the truss that I had designed was statically indeterminate. Luckily for me, I had only wasted an hour of my time trying to determine equation equivalencies and substitutions, which meant that this section took me from 8:40 am to 11:00 am. After today's classes, it'll be back to the drawing board, this time armed with a vital equation for the creation of trusses: 

<img width="591" height="61" alt="image" src="https://github.com/user-attachments/assets/dbc479b2-8717-4ea2-9587-dc5725c2c528" />
[1]

 One might notice that I didn't have to create a new citation for this image. That's because it's out of the same textbook section that I had cited earlier! That's right, I totally missed one of the most important considerations when creating trusses. My only excuse was that I used the site "https://www.truzme.com/free-truss-calculator" to ensure my truss would function correctly under the given loads, and everything worked out on that program. Now, looking back, I understand that the truss calculator uses more than just static equilibrium to determine internal forces. I will provide my work for the indeterminate truss here, so that I may be an example to others of what NOT to do!

<img width="2366" height="3114" alt="A2 Indet Work" src="https://github.com/user-attachments/assets/5812a18e-0f88-4f12-9ed0-b83369c9c04d" />

## Step 1.1:

Truss Modification:

 Now, running low on time, my priority was to keep the majority of the truss I had started with, but modify it to match it to the determinate truss equation. Since I have three reaction forces, my truss must follow the equation: 2J = 3 + M. Right now, my joints and members were not governed by this formula, leaving me with the equation: 12 = 3 + 10. This meant that removing one member would allow my truss to work! I chose to eliminate member FD, leaving me with this new and determinate design:

<img width="2343" height="1048" alt="A2 Truss Modification" src="https://github.com/user-attachments/assets/7a089012-5798-4a44-bb0b-2be07571db44" />

 Now I can actually find all of the internal truss forces and move on. This time I will work from the right side of the truss to the left, since the forces on the right side are easier to determine initially. Here are my final truss calculations:

<img width="2429" height="3169" alt="Final Truss Calc 1" src="https://github.com/user-attachments/assets/bcd65f75-fc98-4529-a4cd-16d5a6a7493b" />
<img width="2322" height="2050" alt="Final Truss Calc 2" src="https://github.com/user-attachments/assets/f7d83de3-d091-4b19-b838-21bc09a1e93d" />

## Step 2:

Cross-Sectional Area and Truss Weight Estimate

Section 2 of the assignment mandates the calculation of the cross-sectional area of the truss beams based on the largest force experienced by one of the truss members and a safety factor of 3.5. During this process, I chose to make the shape of my truss beams rectangular prisms to aid in simplifying both the required area calculations and to make modeling the truss in a CAD program simpler. I am going to employ yield strength as the maximum allowable stress because that is standard practice within engineering. I chose to use grade B A500 steel because its yield strength and tensile strength lie near the middle of the different grades. The yield strength I used was 290 MPa, which was sourced from the site https://www.tottentubes.com/astm-a500-specification-information.

<img width="2406" height="3171" alt="A2 Required Cross Sectional Area" src="https://github.com/user-attachments/assets/692b571c-a965-428c-b2ff-661606381741" />

Based on my calculations, the required area to fulfill the specifications designated by the assignment is 268.2 mm^2. The weight I estimate for my truss design with this cross-sectional area is 79.95N.

## Step 3:

Cross-Sectional Area of Pins

Step three assigns a similar problem as step 2, but is in reference to the pins that hold the truss together, rather than the members it is composed of. Shear stress will be the relevant mode of failure in this scenario, due to a perpendicular load being applied to the pins, rather than the axial one that was applied to the rods. The information we are provided on the pin material (hardened tool steel) is written in U.S. measurements, so it is vital to convert these measurements to standard units. For Ksi, I looked up a conversion factor and manually did the calculation. For converting lb/in^3 to kg/m^3, I used this calculator: https://www.unitconverters.net/density/pound-cubic-inch-to-kilogram-cubic-meter.htm to save some time and ensure I didn't mess up anything in the conversion process. I chose joint D to model my FBD around, but the modelling is strictly for visual purposes. With the way that we determine equilibrium, if I were to sum the forces on any joint, it would add to zero. Therefore, I will make the assumption that the member with the largest load (in my case, member ED that carries 22.22 kN) directly translates that maximum load to the joint. I will solve for the resultant shear force and the necessary cross-sectional area based on this force measurement. A simplification has also been employed to determine the length of the pins - in a real application, they would have to be around 4x the width of the members. Rather than maintain such long pins, and to better align with the weight that will be generated by SolidWorks, I made the decision to model the length of the pins as equal to the width of the members.

<img width="2371" height="3023" alt="A2 Cross Sectional Area of Pins" src="https://github.com/user-attachments/assets/612fba86-6516-4d46-84b9-b48bcc06b3ba" />

## Step 4:

When designing the truss in SolidWorks, I chose to model the truss and the pins in separate files. There was no need to assemble the system, and since the pin and truss materials are of very similar density, there is no point in inserting the pins into the truss inside the modeling program. After designing my truss, I chose AISI 1035 Steel (SS) in the SolidWorks material presets to best mimic the properties of A500 steel. Once I analyzed the resulting mass properties, I found that SolidWorks simulates the actual mass of the truss as 8027.43 grams, or 8.027 kg. This means that my initial estimate of 8.16kg had a percent error of 1.62%, which I am more than happy with! The slight difference is likely due to differences in exact material properties. My weight estimate for the pin was also fairly accurate, with SolidWorks reporting a pin mass of 9.76 g (which, when multiplied by 6 to match the number of joints in my truss, results in a mass of 58.56 grams), while my measurement was 57 grams. That leads to a percent error of 2.74%, which is also acceptable. 

Truss CAD Images:
<img width="2560" height="1440" alt="A2 Truss SS" src="https://github.com/user-attachments/assets/92bef881-f305-4f1d-8a7a-304a6539c831" />
<img width="1936" height="970" alt="A2 Truss Mass Properties SS" src="https://github.com/user-attachments/assets/02abaaf7-9043-4039-8ca0-aff6cb3e2105" />

Pin CAD Images:
<img width="2557" height="1440" alt="A2 Pin SS" src="https://github.com/user-attachments/assets/1244230e-91f0-42f3-8605-9d52dd468e5a" />
<img width="1536" height="1057" alt="A2 Pin Mass Properties SS" src="https://github.com/user-attachments/assets/f09bde20-03bf-4202-86a5-2b1aa7a35da6" />

Percent Error Calculations (Along with Radius Calculation for Pin)
<img width="2804" height="2234" alt="A2 Percent Error Calculations" src="https://github.com/user-attachments/assets/a1576d66-bf87-420c-9c7c-9352aae1576f" />

## Step 5:

The engineering lessons I learned from this lesson are multitudinous and invaluable. Firstly, I understood the importance of fully reading textbook content rather than skimming through it, especially when learning a new topic or refreshing my memory regarding an old one. If I had placed more emphasis on doing this in the first place, I wouldn't have wasted so much time trying to determine a solution to an indeterminate system. On a more positive note, I learned the importance of having a variety of skills when in an engineering design environment. I wouldn't have been able to complete this project as well as I did if I didn't have the math, writing, and computer skills that I have learned throughout my life.

Overall, this project took me about 14 hours.

## Step 5:

2157 Addition:

The article I chose to conduct my research on was https://www.xometry.com/resources/materials/types-of-stress/. It goes over the different types of stresses that can affect materials and how different materials react to such loading types. This is a perfect article for learning about how to determine the likelihood of different failure modes in truss components.

For any of the beams that are experiencing compressive forces- BC, DC, EF, AF, and especially EC, since it supports the highest compression load- the anticipated mode of failure will be buckling. Shortening will also occur due to compressive stress, but the result of excessive shortening is the buckling phenomenon, where the material suddenly folds over and breaks.

For the beams that undergo tensile stress- BE, ED, and DA- rupture/fracture is the anticipated failure mode [2]. A material will resist stretching most effectively prior to its yield point and will return to its original shape as long as it doesn't experience any creep. Beyond this point, the beams of the truss will permanently deform and eventually fracture, causing the system to fail.

To determine the 

ASME Citation: [2]Conniff, M., 2026, “Types of stress in mechanics and materials,” Xometry [Online]. Available: https://www.xometry.com/resources/materials/types-of-stress/. [Accessed: 03-Sep-2026]. 
