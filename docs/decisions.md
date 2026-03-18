# Engineering Decisions

## 2026-03-18

### Decision
Pause the phototransistor approach and test a photoresistor-based route instead.

### Reason
The phototransistor did not provide sufficient voltage separation under current light conditions. Increasing pull-up resistance led to saturation instead of useful improvement.

### Impact
The sensing strategy shifts from direct digital-style detection toward analog sensing with ADC support.

---

### Decision
Use a resistor network to shift the signal into a better ADC range.

### Reason
Measured signal levels were above the most useful operating range for the ESP32-C3 ADC.

### Impact
Signal conditioning becomes part of the hardware front-end design.
