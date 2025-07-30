# 12V-to-220V-DC-Booster

# Boost Converter with PWM Control Using NE555

This project implements a simple boost (step-up) converter using a 555 timer IC as a PWM generator, an IRF540 MOSFET as the power switch, and voltage feedback for output regulation.

## 📷 Circuit Diagram

![Boost Converter Circuit](./<image-name>.png) <!-- Rename the image file and update the name here -->

## ⚙️ Components Used

- **U1**: NE555 – PWM generator
- **Q1**: IRF540 – Power MOSFET
- **Q2**: BC547 – NPN transistor for feedback control
- **D1**: 1N4372A – Zener diode for voltage reference
- **D2**: 3EZ240D5 – High-voltage Zener diode
- **D4**: UF4004 – Fast recovery diode
- **L1**: 470 µH – Power inductor
- **C1**: 470 nF – Timing capacitor for the 555
- **C2**: 10 nF – Decoupling capacitor
- **C4**: 100/250V µF – Output filter capacitor
- **R1, R2, R3** – Timing resistors for the 555
- **R4** – Output pull-down resistor
- **RV1** – Potentiometer for output voltage adjustment
- **Input voltage source**: 12 V DC

## ⚡ How It Works

This circuit functions as a boost converter, stepping up the input voltage from 12 V to an adjustable high-voltage output (~256 V in this example). The NE555 operates as a PWM generator controlled by feedback from the output voltage.

1. The 555 generates pulses to switch the MOSFET (Q1).
2. Inductor L1 stores energy while the MOSFET conducts.
3. When the MOSFET turns off, the stored energy is transferred to the output capacitor (C4) through diode D4.
4. The output voltage is compared with the Zener diode (D1) and dynamically adjusted using transistor Q2, which interferes with the 555’s duty cycle.
5. Potentiometer RV1 allows you to set the output voltage threshold.

## 🔬 Applications

- Adjustable power supplies
- High-voltage LED drivers
- Power systems for Nixie tubes or VFD displays
- Educational power electronics projects

## ⚠️ Warnings

- The output voltage can exceed 250 V. **Handle with extreme care**, especially during real-world testing.
- Ensure all components are rated for the required voltage.
- Always use overcurrent and overvoltage protection in practical implementations.

## 📁 Simulation

This project was simulated in **Proteus**. Include the `.pdsprj` file in the repository folder if you'd like others to run the simulation too.

---

**Author:** Wesley Freitas


