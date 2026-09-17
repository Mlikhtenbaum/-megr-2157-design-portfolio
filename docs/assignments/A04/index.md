# A4 – [Topic]


## Objective
Design a motor mount using the (Brushed 24V DC Gear Motor 3.6Kg.cm/46RPM w/ 99.5:1 Planetary Gearbox) that attaches to a rigid wall.

A. Design around yield strength, with a safety factor of 3
B. Design for maximum deflection of .30mm

## Planning:


### Step 1: 

Step one of the planning process was understanding the different requirements that A4 mandates for the motor mount. Firstly, the mount must be strong enough to withstand an applied stress of 300N. Secondly, it mustn't deflect more than .03mm while the 300N force is acting upon it. 

Step two is drawing out the initial design sketches. There are two features that create the overall structure of the motor mount. Feature 1 is the part of the mount that the motor attaches to. Once the motor is bolted on, it is fixed and has reaction forces in the x and y axes, and a reaction moment that resists applied torque. Feature 2 is mounted to the wall/ceiling and keeps the whole structure in place. Shear stress will be the most important consideration when creating this feature because Feature 1 applies a force to a relatively small area of Feature 2. Deflection is not as important a consideration in the design of Feature 2 due to where the 300N force is being applied, but it must still be accounted for.

*ADD INITIAL SKETCHES HERE* (5)


## Feature 1:

All hand calculations for Feature 1 were simplified based on three assumptions. The first assumption is that the moments of inertia required to solve the problem are based on rectangular measurements, rather than the circular ones which are given. This will affect calculations, since base and height measurements are not manually converted into radial measurements. The second assumption was that forces act directly on the portion of the motor that is sticking out from the mount - the shaft. The third assumption is that the effective base measurement (b(eff)) of the motor mount will be approximately the same as the necessary diameter for the contact flange of the motor mount and motor.

The first two figures detail the process that I used to determine the necessary diameter of the contact flange that connects the motor mount to the motor. While designing for stress, the dimensions of the motor shaft (to which force P is being directly applied) are used to determine the moment of inertia and the magnitude of the moment that is being applied to the shaft. Determining these values based on the dimensions of the thin shaft provides the design with another layer of safety, because long, thin structures are easier to bend. Once I and M are found, the necessary flange diameter is determined to be the value of the variable "b(eff)". Designing for deflection follows a similar process, although the value of the variable b(eff) is determined through the moment equation in this formula. Upon concluding these two calculation processes, my two answers were an outer flange diameter of 18.5mm and 26.8mm for stress and deflection, respectively.

*ADD Design for Stress F1 Here* (1)
*ADD Design for Deflection F1 Here* (2)

My final choice between these two values was 26.8mm, for two reasons. The first is that 26.8mm more effectively combats deflection and keeps the design from deforming further than .03mm. Secondly, after inspecting the motor dimensions, there would be no way to bolt the motor to the mount with a diameter of 18.5 mm- the distance between the bolt holes of the motor is 22mm.

The third figure details the process behind determining the necessary thickness of the motor mount plate. The assumption has been made that the thickness value gathered from these calculations will apply to both the square body of feature 1 and the flange portion that connects the motor to the mount. This is a valid assumption because: A. the flange does not protrude excessively from the body of the mount, which would create a bending moment, and B. the flange dimensions have already been determined based on allowable stress. The formula for normal stress has been used in the calculations for this segment because the force is assumed to be acting axially, rather than on one end of a cantilever, as it was in the previous portion of the design.

*Add Thickness Calc Based on Stress Here* (3)
*Add Thickness Calc Based on Defl Here* (4)

Between these two resultant thicknesses, t = 13.4mm is the clear winner. It is much higher than the thickness value due to stress, likely due to PETG's relatively high yield strength. A deflection of .03mm is fairly minute, especially when considering a 300N force applied to the end of an 18mm lever, and leads to a higher necessary thickness value.


## Feature 2:

All hand calculations for Feature 2 were simplified based on two assumptions. Firstly, the moment created at point A, at the center of the motor mount flange on Feature 1, can be directly translated vertically to affect Feature 2. Secondly, the width and length of Feature 1 can be used for the width and length of Feature 2. Both dimensions are far over-engineered for stress (as the values determined in the Feature 1 calculations prove), and Feature 2 experiences no deflection, so this assumption is valid. 

*Add Feature 2 Stress Dimensions Here* (6)

A height measurement of 8.37mm for Feature 2 makes sense when compared to the other values determined throughout the design process.


## Isometric Sketch:

For this sketch, the part has been flipped to display a view that provides the most detail.

*ADD isometric View* (7)


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

This project took me about 10 hours. Mainly due to my confusion about how to calculate beam equations with the addition of the motor mount flange, which really wasn't necessary anyway.
