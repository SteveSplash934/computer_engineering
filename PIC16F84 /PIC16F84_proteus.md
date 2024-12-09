If you're using **Proteus**, here's how to translate the schematic into a functional simulation:

---

### Step-by-Step Guide to Create the Circuit in Proteus

#### Components Needed:
1. **PIC16F84** (microcontroller)
2. **Push Button** (momentary switch)
3. **LED** (any color)
4. **Resistors**:
   - 10kΩ (pull-down for the button)
   - 220Ω (current limiting for the LED)
5. **Crystal Oscillator** (4MHz)
6. **Capacitors** (22pF x 2 for the oscillator)
7. **Power Source** (5V DC supply)
8. Wires and a Ground connection.

---

### Steps to Build the Circuit in Proteus:
1. **Launch Proteus** and create a new project.

2. **Add Components**:
   - Use the **Pick Devices** tool and search for the required components.
   - Drag and drop each component onto the workspace.

3. **Connect the LED**:
   - Connect the **RB0** pin of the PIC16F84 to the anode (positive terminal) of the LED through a **220Ω resistor**.
   - Connect the cathode (negative terminal) of the LED to the ground.

4. **Connect the Push Button**:
   - Connect one terminal of the push button to **RA0** (pin 17 of the PIC16F84).
   - Attach a **10kΩ resistor** between RA0 and ground (pull-down resistor).
   - Connect the other terminal of the push button to **5V**.

5. **Add the Clock (Oscillator)**:
   - Place a **4MHz crystal oscillator** between the **OSC1** (pin 16) and **OSC2** (pin 15) pins of the PIC16F84.
   - Connect one **22pF capacitor** from OSC1 to ground and another from OSC2 to ground.

6. **Power the PIC16F84**:
   - Connect **VDD** (pin 14) to a **5V power supply**.
   - Connect **VSS** (pin 5) to ground.

7. **Add the Program (HEX File)**:
   - Double-click the PIC16F84 to open the properties window.
   - Under **Program File**, browse to the compiled `.HEX` file generated from your assembly code.
   - Set the clock frequency to **4MHz** (or as specified in your code).

8. **Finalize the Circuit**:
   - Add wires to connect all components as shown in the schematic.
   - Ensure the power supply and ground are properly connected.

---

### Simulating the Circuit
1. Click the **Run** button to start the simulation.
2. **Test the Behavior**:
   - When the button is not pressed, the LED should remain OFF.
   - When the button is pressed, the LED should turn ON.
   - Release the button, and the LED should turn OFF.

---
