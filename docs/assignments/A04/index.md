# A4 – [Topic]

## Objective
Design a motor mount using the (Brushed 24V DC Gear Motor 3.6Kg.cm/46RPM w/ 99.5:1 Planetary Gearbox) that attaches to a rigid wall.

A. Design around yield strength, with a safety factor of 3
B. Design for maximum deflection of .30mm

## Planning:


## Feature 1:

All hand calculations were simplified based on three assumptions. The first assumption is that the moments of inertia required to solve the problem are based on rectangular measurements, rather than the circular ones which are given. This will affect calculations, since base and height measurements are not directly converted into radial measurements. The second assumption was that forces act directly on the portion of the motor that is sticking out from the mount - the shaft. The third assumption is that the effective "base" measurement of the motor mount will be approximately the same as the necessary diameter for the contact patch of the motor mount and motor.

## Decide

The first decision I made was to make the motor mount out of PETG, which is a stronger filament material than the other options. It is a more brittle material than the other plastics, but since we are working below the yield strength and within .30mm of deflection, there shouldn't be any failures resulting from this property.

Secondly, I chose to design my motor mount to resist bearing stress, rather than tensile or shear stress. Bearing stress on the hole diameter that secures the motor's outer flange will be the most important design consideration.

Thirdly, I chose to flip my visual construction of the motor mount to make it align with the positive x-axis. This makes the problem easier to comprehend based on Cartesian coordinates.

Fourth, for feature 1, I chose to utilize the rectangular moment of inertia of the thin, long motor shaft, rather than the large area of the motor itself. The thinner section bends more easily, resists less stress, and therefore is the most important component to consider in the design.

Fifth, I decided to standardize around millimeters within my calculations. This kept all my numbers understandable throughout the design process.

## Communicate

