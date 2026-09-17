# A4 – [Topic]


## Objective
Design a motor mount using the (Brushed 24V DC Gear Motor 3.6Kg.cm/46RPM w/ 99.5:1 Planetary Gearbox) that attaches to a rigid wall.

A. Design around yield strength, with a safety factor of 3

B. Design for maximum deflection of .30mm


### Initial Planning: 

Step one of the planning process was understanding the different requirements that A4 mandates for the motor mount. Firstly, the mount must be strong enough to withstand an applied stress of 300N. Secondly, it mustn't deflect more than .03mm while the 300N force is acting upon it. 

Step two is drawing out the initial design sketches. There are two features that create the overall structure of the motor mount. Feature 1 is the part of the mount that the motor attaches to. Once the motor is bolted on, it is fixed and has reaction forces in the x and y axes, and a reaction moment that resists applied torque. Feature 2 is mounted to the wall/ceiling and keeps the whole structure in place. Bending stress will be the most important consideration when creating this feature because the assignment states that "the deflection of the feature attached to the wall is zero". This is likely the case because Feature 2 is fixed to the ceiling throughout its entire area.

Initial Design Sketches: 

<img width="2422" height="2185" alt="A4-5" src="https://github.com/user-attachments/assets/6b46f27c-2ade-4d4d-9b56-4012b1f89fc3" />


## Feature 1:

All hand calculations for Feature 1 were simplified based on three assumptions. The first assumption is that the moments of inertia required to solve the problem are based on rectangular measurements, rather than the circular ones which are given. This will affect calculations, since base and height measurements are not manually converted into radial measurements. The second assumption was that forces act directly on the portion of the motor that is sticking out from the mount - the shaft. The third assumption is that the effective base measurement (b(eff)) of the motor mount will be approximately the same as the necessary diameter for the contact flange of the motor mount and motor.

Figures 1 and 2 detail the process that I used to determine the necessary diameter of the contact flange that connects the motor mount to the motor. While designing for stress, the dimensions of the motor shaft (to which force P is being directly applied) are used to determine the moment of inertia and the magnitude of the moment that is being applied to the shaft. Determining these values based on the dimensions of the thin shaft provides the design with another layer of safety, because long, thin structures are easier to bend. Once I and M are found, the necessary flange diameter is determined to be the value of the variable "b(eff)". Designing for deflection follows a similar process, although the value of the variable b(eff) is determined through the moment equation in this formula. Upon concluding these two calculation processes, my two answers were an outer flange diameter of 18.5mm and 26.8mm for stress and deflection, respectively.

Beam Stress Calculations: Figure 1

<img width="2444" height="3110" alt="A4-1" src="https://github.com/user-attachments/assets/60dfce43-9b6f-487b-b39d-c63aca002a99" />

Beam Deflection Calculations: Figure 2

<img width="2421" height="3100" alt="A4-2" src="https://github.com/user-attachments/assets/45e09fde-9782-4701-869e-75fe08240417" />

My final choice between these two values was 26.8mm, for two reasons. The first is that 26.8mm more effectively combats deflection and keeps the design from deforming further than .03mm. Secondly, after inspecting the motor dimensions, there would be no way to bolt the motor to the mount with a diameter of 18.5 mm- the distance between the bolt holes of the motor is 22mm.

Figures 3 and 4 detail the process behind determining the necessary thickness of the motor mount plate. Figure 3 provides a mount thickness based on the bending stress experienced by the part. Figure 4 uses maximum deflection to determine thickness based on stability rather than stress. The height of Feature 1's flange is not accounted for within this calculation to simplify the computational process. The formula for normal stress has been used in the stress calculations for this segment because the force is assumed to be acting axially, rather than on one end of a cantilever, as was true in the previous portion of the design.

Beam Stress Calculations: Figure 3

<img width="2289" height="3038" alt="A4-3" src="https://github.com/user-attachments/assets/1d0c82da-d83a-4c73-b118-a03a47051d71" />

Beam Deflection Calculations: Figure 4

<img width="2408" height="3176" alt="A4-4" src="https://github.com/user-attachments/assets/d0cc4ac7-0ea4-4bb5-b751-21932f743962" />

Between these two resultant thicknesses, t = 13.4mm is the clear winner. It is much higher than the thickness value due to stress, which is very low due to PETG's relatively high yield strength. A deflection of .03mm is fairly small, especially when considering a 300N force applied to the end of an 18mm lever, and leads to a higher necessary thickness value.


## Feature 2:

All hand calculations for Feature 2 were simplified based on two assumptions. Firstly, the moment created at point A, at the center of the motor mount flange on Feature 1, can be directly translated vertically to affect Feature 2. Secondly, the width and length of Feature 1 can be used for the width and length of Feature 2. Both dimensions are far over-engineered for stress (as the values determined in the Feature 1 calculations prove), and Feature 2 experiences no deflection, so this assumption is valid. 

Beam Stress Calculations:

<img width="2398" height="3147" alt="A4-6" src="https://github.com/user-attachments/assets/2f1fd491-c3e1-491f-a7b7-264d7dbfc85b" />

A height measurement of 8.37mm for Feature 2 makes sense when compared to the other values determined throughout the design process.


## Isometric Sketch:

For this sketch, the part has been flipped to display a view that provides the most detail.

<img width="2332" height="1969" alt="A4-7" src="https://github.com/user-attachments/assets/a093460d-5fe3-4133-a749-97ca54e8b07a" />


## SolidWorks Model:

Throughout this section of A4, I provided screenshots with headings that guide readers through my 3D model design process. I made the decision to add fillets at the joints between certain connections to reduce the magnitude of any stress risers and allow for ease of printing.

Designing Feature 2 came first so that I could mimic the isometric sketch that I had created previously most effectively:

<img width="1623" height="902" alt="Feature 2 sketch" src="https://github.com/user-attachments/assets/b4060bf9-130b-47e6-bcda-80447288ef8f" />

<img width="1997" height="892" alt="Feature 2 extrusion" src="https://github.com/user-attachments/assets/33f732b6-dfd1-4032-bb4e-bb94192ec163" />

Designing Feature 1 came second:

<img width="2347" height="1279" alt="Feature 1 Sketch and Extrusion" src="https://github.com/user-attachments/assets/5d886f61-38b4-4938-bc9b-6be0a4148b26" />

Flange design was third:

<img width="2372" height="1120" alt="Flange Sketch and Extrusion" src="https://github.com/user-attachments/assets/aa62dcc3-3922-4a00-8214-ed4a0a764a24" />

Flange Strength Addition via a fillet feature was fourth:

<img width="2494" height="1187" alt="Flange Fillet" src="https://github.com/user-attachments/assets/0af7360c-cad9-4d1f-851b-80f3a5641998" />

F1 Bolt Holes, fifth:

<img width="1607" height="1078" alt="Bolt hole creation" src="https://github.com/user-attachments/assets/419bd273-6f56-4dbe-bce8-f71908e03b92" />

F2 Bolt Holes and the Shaft Hole came last:

<img width="2515" height="1181" alt="Shaft_Bolt holes" src="https://github.com/user-attachments/assets/8641f1d0-d5f1-4c5f-9b89-78dd0c1d51fa" />


## Drawings:

This technical drawing conveys all features and dimensions needed to replicate my motor mount design.

<img width="1055" height="819" alt="Drawing" src="https://github.com/user-attachments/assets/e14b3963-caac-402f-8765-3786c747cc44" />


## Decisions: 

The first decision I made was to make the motor mount out of PETG, which is a stronger filament material than the other options. It is a more brittle material than the other plastics, but since we are working below the yield strength and within .30mm of deflection, there shouldn't be any failures resulting from this property.

Secondly, I designed a flange for the motor to mount onto, rather than mounting it straight to the rectangular portion of the motor mount. This adds material and makes the design more resistant to bending without having to increase the thickness of the entire square cross-section of Feature 1. This maximizes strength while minimizing filament use and additional weight.

Thirdly, I chose to flip my visual construction of the motor mount to make it align with the positive x-axis. This makes the problem easier to comprehend based on Cartesian coordinates.

Fourth, for feature 1, I chose to utilize the rectangular moment of inertia of the thin, long motor shaft, rather than the large area of the motor itself. The thinner section bends more easily, resists less stress, and therefore is the most important component to consider in the design.

Fifth, I decided to standardize around millimeters within my calculations. This kept all my numbers understandable throughout the design process.

Finally, I chose to offset the height/length of the motor mount flange by 1mm out from the thickness of the motor mount. This is valid because it adds enough material to provide a circular surface for the motor to contact while keeping the leverage of P on the feature to a minimum.


## Communicate

One mistake that I wish I had accounted for was not adding ample length to F1. If this motor mount were produced, there would be no access to the wall-mounting bolts without removing the motor first, which would be a pain.

One of the engineering lessons I learned from this project was carrying units. Due to the complexity of the calculations and the number of variables involved, ensuring that units cancel out is vital to determining correct design dimensions.

This project took me about 11 hours. Mainly due to my confusion about how to calculate beam equations with the addition of the motor mount flange, which really wasn't necessary anyway.

## Downloads:

Here is the [link](https://drive.google.com/drive/folders/1zwv8j4h-NW8Ql2mJCiRN7Nqz18Xc2u2_?usp=drive_link) to the Google Drive folder that contains my CAD file and engineering drawing.
Here is the [A4 Motor Mount Drawing.pdf](https://github.com/user-attachments/files/32320895/A4.Motor.Mount.Drawing.pdf) download.
