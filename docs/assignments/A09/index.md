# A9 – Pulleys

## Objective:

Description:
Design a pulley system to transfer power between two parallel axes separated by a center distance of 4–6 inches. The system must meet the following requirements:

Pulley Diameter: Both pulleys shall have a diameter of 3 inches.
Rotational Speed: Select an operating speed between 1000–2000 rpm.
Belt Tension (Static): Select a belt tension between 4–6 lbf under stationary conditions.
Material: Pulleys may be made from aluminum, ABS, or steel, and may include a groove and shaft diameter of your choosing (within reasonable manufacturing limits).
Safety Factor: The design must satisfy a minimum safety factor of 3.
Assume the belt is made from polyurethane rubber, with a yield strength of 3.25 MPa (471 psi) at 20% strain, based on Wanga, Chena, Wua, Zhangb, Suna, “Strain-induced Structural and Dynamic Changes in Segmented Polyurethane Elastomers.”

<img width="747" height="402" alt="Figure 1 Provided" src="https://github.com/user-attachments/assets/c2a98fd3-6212-44cf-9b05-faeab517152e" />
[General Pulley Structure]

<img width="889" height="467" alt="Appendix 1" src="https://github.com/user-attachments/assets/85570625-7fca-4533-bbf3-6ecf25ebd7c7" />
[Frame Example]



## Decide:

Chosen:
- Center Distance: 5"
- Rotational Speed: 1000 RPM
- Belt Tension: 5 lbf
- Pulley Material: ABS

Given:
- Safety Factor: 3 
- Pulley Diameter: 3"
- Belt Specifications: Polyurethane rubber, with a yield strength of 3.25 MPa (471 psi) at 20% strain

Formulas to Note:

* **Rotational Speed:** $\frac{n_1}{n_2} = \frac{D_2}{D_1} = \frac{D}{D} = 1 \implies n_1 = n_2$
* **Transmitted Torque ($T$):** $T = (F_1 - F_2) \cdot r = \frac{D}{2}(F_1 - F_2)$
* **Simplified Transmitted Torque for Same-Diameter Pulleys:** $T = (F_1 - F_2)r$
* **Power Transmitted ($P$):** $P = T \cdot \omega = T \cdot \left(\frac{2\pi n}{60}\right)$
* **Linear Belt Speed ($v$):** $v = \omega \cdot r = \frac{\pi \cdot D \cdot n}{60}$
* **Round Belt on Flat Pulley Surface:** $\frac{F_1}{F_2} = e^{\mu \theta}$
* **Initial Tension Force:** $F_i = \frac{F_1 + F_2}{2}$



## Analyze:



### Belt Length and Diameter Calculations:

Chosen Belt Diameter and Length to best match calculated values: Round Belt 1/4" Diameter, 19 and 1/4" long (3044K606). The shorter belt length (.175 in shorter) will add slightly more tension, but the resulting safety factor should still be adequate. The coefficient of friction is assumed to be .4 since that is slightly less than the friction coefficient for metal. No publicly accessible graph or database provides static friction coefficients between polyurethane and ABS (or other plastics, for that matter).

<img width="2544" height="3180" alt="Pulley Calc" src="https://github.com/user-attachments/assets/9cb01373-f7f3-472b-a53e-dd03d54364c9" />
[Belt and Pulley Hand Calculations]



### Shaft Calculations: 

Shear yield strength is assumed to be .557(tensile yield) as per Von Mises. The shaft diameter is calculated to be .135in.

<img width="2547" height="3197" alt="Shaft Calc" src="https://github.com/user-attachments/assets/fb8b09f9-5e0d-4b8b-a183-4bb1c3c8b115" />
[Shaft Hand Calculations]



### Journal Bearing Calculations:

The minimum diameter value calculated in the previous section is not provided as a journal bearing size on McMaster, so the shaft diameter is increased to match the 5/32 journal bearing ID size. Based on Table 4 provided in the Machinery's Handbook, porous bronze is more than capable of taking on the loads applied by the pulley system. The length-to-diameter ratio used for these calculations was 1, to establish adequate contact between the bearing and shaft. Thus, a 5/32" bearing length was used in the following hand calculations. In reality, a 1/4" long bearing would be sourced and used, which would lower the PV calculation even further.

<img width="792" height="582" alt="image" src="https://github.com/user-attachments/assets/e5e8a903-e895-4627-be8e-4dc48ab884af" />
[Machinery's Handbook Page 2440 Table 4]

<img width="2583" height="3278" alt="Bearing Calc" src="https://github.com/user-attachments/assets/3f919a08-77bd-4de6-960b-503e6318c01d" />
[Journal Bearing Hand Calculations]



### Frame Design:

The creation of a SolidWorks Frame model is detailed here. A frame thickness of 1/4in and an outer bearing diameter of 1/4in is used to best model the bearing dimensions available on McMaster-Carr. A width of 1/4in is used on the outer sections of the frame to support the load created by the pulley shafts. The frame material is ABS, as the applied force is relatively low. The stress analyzed in the hand calculation was bearing bore contact, as it is a likely failure mode for the part.

<img width="2395" height="3151" alt="Frame Calc" src="https://github.com/user-attachments/assets/11699a39-ec0d-4ecb-9d83-e325d30514d7" />
[Frame Hand Calculations]

<img width="778" height="723" alt="image" src="https://github.com/user-attachments/assets/341cf9c6-be41-4da8-b9fb-344500be95ec" />
[Global Variable Creation]

<img width="1896" height="1007" alt="image" src="https://github.com/user-attachments/assets/5a780e39-719c-4fb9-b5a7-a3a603a468d7" />
[Initial Sketch]

<img width="1901" height="1004" alt="image" src="https://github.com/user-attachments/assets/c664601d-8fd5-4285-87d0-7a63c2e8cf3b" />
[Part Extrusion]

<img width="1427" height="726" alt="image" src="https://github.com/user-attachments/assets/118503ee-dbf8-47fc-813c-325a8075d8e3" />
[Final Frame Design]



## Communicate:
- One engineering lesson I learned from this project was the usefulness of having a standard length-to-diameter ratio to estimate unknown values and ensure that forces are distributed evenly. I also learned about the force relationships found within pulley systems, which are initially counterintuitive. The project took me about 5 hours.
- Google Gemini was used to code the prettyprint formulas in the "Decide:" section.
- [Belt Link](https://www.mcmaster.com/3044K606-1835T382/)
- [Frame CAD Download](https://drive.google.com/drive/folders/1vA55Cm_CcWHrtvSAhfnMFiWjdIQkby19?usp=sharing)
