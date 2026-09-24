<img width="4000" height="3000" alt="9" src="https://github.com/user-attachments/assets/0da5b5fa-30c8-4611-8210-673b7ec9c0e5" /># A5 – Bracket Design


## Objectives:

### All Sections:

Detail-design a bracket by analyzing the normal stress, bending stress, and stiffness equations using strength of materials to determine dimensions. Use statics and solid mechanics skills to complete the task of designing the features.

- Conduct stress analysis to determine appropriate dimensions for structural features.
- Generate free-body diagrams (FBDs) to visualize forces and constraints for each feature.
- Identify and document known and unknown variables, assumptions, and algebraic models for stress calculations.
- Perform stiffness analysis to establish minimum required dimensions based on deflection constraints.
- Compare stress and stiffness analyses to ensure structural integrity and compliance with given constraints.
- Create detailed multiview sketches illustrating dimensions derived from both stress and stiffness analyses.
- Reflect on and document key engineering lessons learned throughout the process.

### 2157 Additions:

Design a link (Appendix E) that connects feature A to another cylindrical feature, such that the connection can hold using the same amount of force. The link is to be made from one of the three specified metals.

- The hole in the link that connects to feature A must be designed as a running/sliding fit.
- The hole in the link that connects to the 1-inch diameter shaft must be designed with light assembly pressure.

Design the dimensions of the link:

- Use stress/strength equations to determine the required cross-sectional area of the linkage, focusing on the smallest cross-sectional area at the holes.
- Apply the axial deflection equation to verify both the cross-sectional area and the length of the linkage, again considering the smallest cross-sectional area at the holes.

Select the proper fit for feature A and for the 1" shaft:

- Discuss the design process used, and cite resources (include page numbers) in your documentation.
- Select the proper manufacturing technique. Show the process included tables used.


## Planning:

### Step 1:
The first step of this project is understanding exactly what objects and forces are relevant to consider when designing the dimensions of the bracket shaft. A polyester strap will wrap around the shaft area of the bracket and pull down with a force of 2F. This means that the shaft must be long enough to support the full width of the strap, and strong enough to resist the deflection and stress caused by the applied force. The rest of the overall bracket geometry is provided within Appendix B: 

<img width="1255" height="812" alt="Appendix B" src="https://github.com/user-attachments/assets/4f1504ff-085d-4c07-97e4-c4e6be3cc926" />

An important consideration to note prior to sketching and designing the bracket for this section is that the strap will apply a horizontal force, rather than the vertical one detailed by Appendix B.

### Step 2:
The second step of the design will be sketching out the overall geometry of the part. We are provided with enough information about the different part segments and the necessary connections to draw out an overall design.

### Step 3:
The second phase entails creating FBD's of every relevant section of the bracket and considering the applied stress to determine necessary segment dimensions. The modulus of elasticity of Steel (ASTM A36) must be used for this section, and a safety factor of 4 is to be employed. 

### Step 4:
The third step involves creating the same FBDs as the previous section and determining bracket dimensions through strain analysis. Each segment of the bracket must fall within a maximum deflection of 5 thousandths of an inch.


## Action Phase:

### Reference Sketch:

<img width="4000" height="3000" alt="1" src="https://github.com/user-attachments/assets/a36a4acf-0e8c-455f-b5ad-e87e9af05cda" />

The height of B is the same for both strategies because it must be within 16" to meet the required maximum deflection. Therefore, it was adjusted to 0.5" (when measuring from shaft center to bottom of bracket body) to accommodate the required shaft dimension and allow space for the strap.


### Stress Analysis:
This section details the symbolic formulas and numeric calculations used to determine necessary bracket dimensions based on an allowable stress of 9000N. 

<img width="4000" height="3000" alt="2" src="https://github.com/user-attachments/assets/f0f4ea54-97e9-4d39-ba94-a62d246e6abe" />

<img width="4000" height="3000" alt="3" src="https://github.com/user-attachments/assets/868b85f8-83fb-40ed-8d98-0a198f3fdbaf" />

<img width="4000" height="3000" alt="4" src="https://github.com/user-attachments/assets/9e36b3a7-ad52-4491-a6c3-8a97cdafe7f4" />

<img width="4000" height="3000" alt="5" src="https://github.com/user-attachments/assets/2fb0287c-673f-4916-b890-bb11f2670459" />

<img width="4000" height="3000" alt="6" src="https://github.com/user-attachments/assets/deb38074-6750-41c6-b4dc-abedbfe62b5c" />

### Deflection Analysis:

This section details the symbolic formulas and numeric calculations used to determine necessary bracket dimensions based on a maximum deflection of .005". FBDs have been simplified to increase efficiency. Refer to the previous subheading "Stress Analysis" for more detailed FBD's.

<img width="4000" height="3000" alt="7" src="https://github.com/user-attachments/assets/aa38d720-40eb-463e-8d41-0dd2fb188ab6" />

<img width="4000" height="3000" alt="8" src="https://github.com/user-attachments/assets/54db83c1-2cf3-4ec2-9899-8fa52d955850" />

<img width="4000" height="3000" alt="9" src="https://github.com/user-attachments/assets/766b814c-c134-4859-9747-b079b3c829aa" />

<img width="4000" height="3000" alt="10" src="https://github.com/user-attachments/assets/0ddbf844-6f4e-4a49-a470-71b768d5343c" />

<img width="4000" height="3000" alt="11" src="https://github.com/user-attachments/assets/74ff7b1b-d3c3-4320-a639-ad33a73b815a" />

### Multiview Drawings:

<img width="4000" height="3000" alt="12" src="https://github.com/user-attachments/assets/77451caa-8570-4176-a9b6-564eeaf868bc" />

<img width="4000" height="3000" alt="13" src="https://github.com/user-attachments/assets/0b97196b-f835-40d3-b69a-3f09067e6506" />


## Lessons Learned:

Governing failure mode: For feature A of the bracket, the strap shaft has a governing failure mode of stress due to bending. Stress governed its final dimension of a diameter of .726", since deflection required a smaller diameter of .3652". Stress required nearly twice as much support from the feature, likely due to the small overall size of the part.

Error propagation: One instance where a value from an earlier feature carried into a later one was the diameter of feature A becoming the length of feature B. There were no errors that occurred throughout the calculation process because I double-checked my dimensional analysis.

Assumption sensitivity: One assumption I made was that a height of feature B (the axially loaded bar that attaches feature A to the rest of the bracket) could be assumed to be .5", since it was well within the height dictated by maximum deflection, and would allow the other bracket segments to be smaller as well. If this was determined to be incorrect, say if the user needed to use a much thicker strap, this dimension would have to be increased.

## 2157 Addition:



## Decide:

One of the first decisions I made after reading the assignment instructions was to design a perfectly symmetrical bracket and assume that no failure will occur due to direct shear stress. These considerations will simplify the design and its associated calculations.

The second decision I made was to design my bracket entirely using Steel (ASTM A36). I chose this design for a few reasons. First, steel is strong, and using it will allow my design to be slightly smaller than one made of aluminum (when considering stress). Secondly, steel is relatively cheap and will keep the manufacturing price low. Third, using one material throughout the design simplifies the calculations needed to determine press-fit dimensions.

Thirdly, when analyzing features D and E based on stress, I modelled them as bars rather than beams. This is a more accurate strategy because the heights of both features are much more substantial than their length. This means that they bend very little, and linear stress/deformation is a more important consideration.


## Communicate

