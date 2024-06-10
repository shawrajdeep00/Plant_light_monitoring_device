# Plant Light Monitoring Device

## Overview

This repository provides the code and instructions to set up a Light Intensity Monitoring System using the Bolt IoT module. The system uses an LDR (Light Dependent Resistor) to measure light intensity and visualize the data on the Bolt Cloud.

## Hardware Required

- 1 x Bolt IoT Module
- 1 x Micro USB Cable
- 1 x LDR (Light Dependent Resistor)
- 1 x 10k Ohm Resistor (brown black orange color code)

The resistance of an LDR varies inversely with light, i.e., the resistance decreases as the intensity of light falling on the LDR increases.

## Hardware Connections

### Safety Note
Always power off the Bolt module while making connections to ensure your safety and the safety of the circuit. Double-check all connections before powering it on.

### Steps for Making the Hardware Connections

1. **Insert the LDR:**
    - Insert one lead of the LDR into the Bolt Module's 3.3V pin.
    - Insert the other lead of the LDR into the A0 pin.

2. **Insert the 10k Ohm Resistor:**
    - Insert one leg of the 10k Ohm resistor into the GND pin.
    - Insert the other leg of the resistor into the A0 pin.

Ensure that at no point do the 3.3V (or 5V) and GND pins or wires touch each other. If power and ground are shorted without a resistor, the current might be high enough to destroy the Bolt module.

### Final Circuit

The final circuit effectively measures the voltage across the 10k Ohm resistor. It should look like the image below:

![Circuit Diagram]("C:\Users\Rajdeep Shaw\Downloads\bolt_iot_LDR.jpg")

## Software Setup

### Configuring Bolt Cloud

1. Create a new product on the Bolt Cloud.
2. Configure the A0 pin as an input to read the light intensity.
3. Link the product to the device

### JavaScript Code

Use the following JavaScript code to plot the light intensity values along with timestamps on the Bolt Cloud:

```javascript
plotChart("time_stamp", "light");
```

## Usage

1. Power on the Bolt IoT module after making all the connections.
2. Monitor the light intensity data on the Bolt Cloud dashboard.

## Conclusion

This Light Intensity Monitoring System using Bolt IoT provides a simple yet effective way to measure and visualize light intensity. By following the instructions and using the provided code, you can set up your own monitoring system with ease.
