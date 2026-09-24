# A5 – Bracket Design


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

The height of B is the same for both strategies because it must be within 16" to meet the required maximum deflection. Therefore, it was adjusted to 0.5" (when measuring from shast center to bottom of bracket body) to accommodate the required shaft dimension and allow space for the strap.

### Stress Analysis:
This section details the symbolic formulas and numeric calculations used to determine necessary bracket dimensions based on an allowable stress of 9000N. 

### Deflection Analysis:

This section details the symbolic formulas and numeric calculations used to determine necessary bracket dimensions based on a maximum deflection of .005". FBDs have been simplified to increase efficiency. Refer to the previous subheading "Stress Analysis" for more detailed FBD's.



## Decide:

One of the first decisions I made after reading the assignment instructions was to design a perfectly symmetrical bracket and assume that no failure will occur due to direct shear stress. These considerations will simplify the design and its associated calculations.

The second decision I made was to design my bracket entirely using Steel (ASTM A36). I chose this design for a few reasons. First, steel is strong, and using it will allow my design to be slightly smaller than one made of aluminum (when considering stress). Secondly, steel is relatively cheap and will keep the manufacturing price low. Third, using one material throughout the design simplifies the calculations needed to determine press-fit dimensions.

Thirdly, when analyzing features D and E based on stress, I modelled them as bars rather than beams. This is a more accurate strategy because the heights of both features are much more substantial than their length. This means that they bend very little, and linear stress/deformation is a more important consideration.


## Communicate

