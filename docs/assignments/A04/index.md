# A4 – [Topic]

## Objective
Design a motor mount using the (Brushed 24V DC Gear Motor 3.6Kg.cm/46RPM w/ 99.5:1 Planetary Gearbox) that attaches to a rigid wall.

A. Design around yield strength, with a safety factor of 3
B. Design for maximum deflection of .30mm

## Planning:

### Step 1: 

Step one of the planning process was understanding the different requirements that A4 mandates for the motor mount. Firstly, the mount must be strong enough to withstand an applied stress of 300N. Secondly, it mustn't deflect more than .03mm while the 300N force is acting upon it. 

Step two is drawing out the initial design sketches. There are two features that create the overall structure of the motor mount. Feature 1 is the part of the mount that the motor attaches to. Once the motor is bolted on, it is fixed and has reaction forces in the x and y axes, and a reaction moment that resists applied torque. Feature 2 is mounted to the wall/ceiling and keeps the whole structure in place. Shear stress will be the most important consideration when creating this feature because Feature 1 applies a force to a relatively small area of Feature 2. Deflection is not as important a consideration in the design of Feature 2 due to where the 300N force is being applied, but it must still be accounted for.

## Feature 1:

All hand calculations for Feature 1 were simplified based on three assumptions. The first assumption is that the moments of inertia required to solve the problem are based on rectangular measurements, rather than the circular ones which are given. This will affect calculations, since base and height measurements are not manually converted into radial measurements. The second assumption was that forces act directly on the portion of the motor that is sticking out from the mount - the shaft. The third assumption is that the effective base measurement (b(eff)) of the motor mount will be approximately the same as the necessary diameter for the contact flange of the motor mount and motor.

The first two figures detail the process that I used to determine the necessary diameter of the contact flange that connects the motor mount to the motor. While designing for stress, the dimensions of the motor shaft (to which force P is being directly applied) are used to determine the moment of inertia and the magnitude of the moment that is being applied to the shaft. Determining these values based on the dimensions of the thin shaft provides the design with another layer of safety, because long, thin structures are easier to bend. Once I and M are found, the necessary flange diameter is determined to be the value of variable "b(eff)". Designing for deflection follows a similar process, although the value of variable b(eff) is determined through the moment equation in this formula. Upon concluding these two calculation processes, my two answers were an outer flange diameter of 18.5mm and 26.8mm for stress and deflection, respectively.

*ADD Design for Stress F1 Here*
*ADD Design for Deflection F1 Here*

My final choice between these two values was 26.8mm, for two reasons. The first is that 26.8mm more effectively combats deflection and keeps the design from deforming further than .03mm. Secondly, after inspecting the motor dimensions, there would be no way to bolt the motor to the mount with a diameter of 18.5 mm- the distance between the bolt holes of the motor is 22mm.

The third figure details the process behind determining the necessary thickness of the motor mount plate 

## Feature 2:

All hand calculations for Feature 2 were simplified based on two assumptions. 

## Decide

The first decision I made was to make the motor mount out of PETG, which is a stronger filament material than the other options. It is a more brittle material than the other plastics, but since we are working below the yield strength and within .30mm of deflection, there shouldn't be any failures resulting from this property.

Secondly, I chose to flip my visual construction of the motor mount to make it align with the positive x-axis. This makes the problem easier to comprehend based on Cartesian coordinates.

Thirdly, for feature 1, I chose to utilize the rectangular moment of inertia of the thin, long motor shaft, rather than the large area of the motor itself. The thinner section bends more easily, resists less stress, and therefore is the most important component to consider in the design.

Fourth, I decided to standardize around millimeters within my calculations. This kept all my numbers understandable throughout the design process.

## Communicate

