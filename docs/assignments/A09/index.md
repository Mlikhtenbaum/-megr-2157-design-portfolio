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

**Rotational Speed:**
$$
\frac{n_1}{n_2} = \frac{D_2}{D_1} = \frac{D}{D} = 1 \implies n_1 = n_2
$$

**Transmitted Torque ($T$):**
$$
T = (F_1 - F_2) \cdot r = \frac{D}{2}(F_1 - F_2)
$$

**Simplified Transmitted Torque for Same Diameter Pulleys:**
$$
T = (F_1 - F_2)r
$$

**Power Transmitted ($P$):**
$$
P = T \cdot \omega = T \cdot \left(\frac{2\pi n}{60}\right)
$$

**Linear Belt Speed ($v$):**
$$
v = \omega \cdot r = \frac{\pi \cdot D \cdot n}{60}
$$

**Flat Belts:**
$$
\frac{F_1}{F_2} = e^{\mu \theta}
$$


## Analyze:




## Communicate:

- Google Gemini was used to code in the prettyprint formulas in the "Decide:" section.
