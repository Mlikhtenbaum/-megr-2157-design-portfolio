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

<img width="2569" height="1964" alt="1" src="https://github.com/user-attachments/assets/25b764ee-2d71-489c-b5c7-356715ea6259" />

The height of B is the same for both strategies because it must be within 16" to meet the required maximum deflection. Therefore, it was adjusted to 0.5" (when measuring from shaft center to bottom of bracket body) to accommodate the required shaft dimension and allow space for the strap.


### Stress Analysis:
This section details the symbolic formulas and numeric calculations used to determine necessary bracket dimensions based on an allowable stress of 9000N. 

<img width="2278" height="2851" alt="2" src="https://github.com/user-attachments/assets/724e66d1-bacb-4c69-a1e6-b0c4bfb5cd57" />

<img width="2274" height="2937" alt="3" src="https://github.com/user-attachments/assets/e8d56da4-a206-493d-b007-4a9e35e6aac2" />

<img width="2222" height="2835" alt="4" src="https://github.com/user-attachments/assets/e6c83419-03f2-4035-aec8-fa0b6e6a1d35" />

<img width="2235" height="2734" alt="5" src="https://github.com/user-attachments/assets/23e11448-79da-4431-b412-7e78cf78077e" />

<img width="2287" height="2881" alt="6" src="https://github.com/user-attachments/assets/58ca0c6a-51ec-4411-93c7-2a9213159dba" />

### Deflection Analysis:

This section details the symbolic formulas and numeric calculations used to determine necessary bracket dimensions based on a maximum deflection of .005". FBDs have been simplified to increase efficiency. Refer to the previous subheading "Stress Analysis" for more detailed FBD's.

<img width="2428" height="3101" alt="7" src="https://github.com/user-attachments/assets/bcfa113d-62c6-4361-8535-70c4a331a875" />

<img width="2400" height="3002" alt="8" src="https://github.com/user-attachments/assets/b85b9920-ecc8-48ff-9a65-9f6918c0c258" />

<img width="2445" height="3136" alt="9" src="https://github.com/user-attachments/assets/6f2c5d82-aafe-49cb-a177-e3346c202846" />

<img width="2263" height="2875" alt="10" src="https://github.com/user-attachments/assets/5c2a9c86-1e3d-46eb-9085-190852928451" />

<img width="2436" height="3068" alt="11" src="https://github.com/user-attachments/assets/9b442d06-2b56-48a8-a080-958a026cd195" />

### Multiview Drawings:

<img width="2628" height="3147" alt="12" src="https://github.com/user-attachments/assets/2dc958ca-b8f1-4065-b100-9496669d2e62" />

<img width="2374" height="2942" alt="13" src="https://github.com/user-attachments/assets/4420e368-a6d6-46e4-998b-9f40ef3b04ba" />


## Lessons Learned:

Governing failure mode: For feature A of the bracket, the strap shaft has a governing failure mode of stress due to bending. Stress governed its final dimension of a diameter of .726", since deflection required a smaller diameter of .3652". Stress required nearly twice as much support from the feature, likely due to the small overall size of the part.

Error propagation: One instance where a value from an earlier feature carried into a later one was the diameter of feature A becoming the length of feature B. There were no errors that occurred throughout the calculation process because I double-checked my dimensional analysis.

Assumption sensitivity: One assumption I made was that a height of feature B (the axially loaded bar that attaches feature A to the rest of the bracket) could be assumed to be .5", since it was well within the height dictated by maximum deflection, and would allow the other bracket segments to be smaller as well. If this was determined to be incorrect, say if the user needed to use a much thicker strap, this dimension would have to be increased.

## 2157 Addition:

### Linkage Design and Area Calculation:

The overall length of the part is assumed to be 3" to account for hole cutouts and required part thickness. This is a known valid assumption because of a previous calculation completed for feature B, which dictated that a part with a similar cross-sectional area must lie within 16". The linkage is made from the same ASTM A36 Steel as the bracket for simplicity. Shear stress is disregarded to better match the format of calculations employed in previous sections.

<img width="2448" height="3158" alt="14" src="https://github.com/user-attachments/assets/82e7b28d-b3c7-4f33-9cd9-2602a9b8ec66" />

### .726" D Hole Callout:

The hole in the link that connects to feature A must be designed as a running/sliding fit. Based on this specification, I have assumed that an RC7 fit is adequate, due to the likelihood of such a strap being used in an outdoor environment. An RC7 fit dictates that the .726" diameter hole of the linkage must lie within a tolerance of +.002", -.000". Feature A, which interfaces with this hole, must be .726" and lie within a tolerance of -.0025" to -.0037". An RC7 fit is classified as tolerance grade 9, meaning the hole can be manufactured using the reaming process.

<img width="1097" height="468" alt="726 D Tolerance" src="https://github.com/user-attachments/assets/442b527f-8e5f-46b0-8f63-78df18381bea" />
This clearance information can be found on page 654 of the Machinery's Handbook

### 1.000" D Hole Callout:

The hole in the link that connects to the 1-inch diameter shaft must be designed with light assembly pressure. Based on this information, an FN2 fit is adequate, considering it is described as a fit "suitable	for	ordinary	steel	parts" on page 651 of the Machinery's Handbook. An FN2 fit dictates that the 1.000" diameter hole of the linkage must lie within a tolerance of +.0008", -.000". The 1" cylinder, which interfaces with this hole, must be 1" and lie within a tolerance of +.0014" to +.0019". Reaming can also create this hole, since an FN2 fit is within tolerance grade 7.

<img width="792" height="575" alt="1 D Tolerance" src="https://github.com/user-attachments/assets/5ab48987-885f-427f-9ed2-7e16ca45377c" />
This clearance information can be found on page 658 of the Machinery's Handbook

<img width="1025" height="1158" alt="image" src="https://github.com/user-attachments/assets/7a52b979-b8cf-4881-ba56-d0e1e6a73b9b" />
This tolerance grade chart can be found on  page 649 of the Machinery's Handbook


## Decide:

One of the first decisions I made after reading the assignment instructions was to design a perfectly symmetrical bracket and assume that no failure will occur due to direct shear stress. These considerations will simplify the design and its associated calculations.

The second decision I made was to design my bracket entirely using Steel (ASTM A36). I chose this design for a few reasons. First, steel is strong, and using it will allow my design to be slightly smaller than one made of aluminum (when considering stress). Secondly, steel is relatively cheap and will keep the manufacturing price low. Third, using one material throughout the design simplifies the calculations needed to determine press-fit dimensions.

Thirdly, when analyzing features D and E based on stress, I modelled them as bars rather than beams. This is a more accurate strategy because the heights of both features are much more substantial than their length. This means that they bend very little, and linear stress/deformation is a more important consideration.


## Communicate

This project helped me massively with understanding and using tolerance charts and determining proper manufacturing and design techniques. Overall, it took me about 13 hours.
