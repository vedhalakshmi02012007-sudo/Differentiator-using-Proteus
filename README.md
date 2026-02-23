## Experiment No: 3
DIFFERENTIATOR USING OP-AMP (μA741)
## Aim
To design and simulate a Differentiator circuit using μA741 in Proteus Design Suite and verify that the output is proportional to the rate of change of input voltage.
## Apparatus Required

•	μA741 Op-Amp

•	Capacitor C = 0.01 µF

•	Resistor Rf = 10 kΩ

•	Signal Generator

•	Dual Power Supply (±12V)

•	CRO / Oscilloscope

•	Connecting wires

## Circuit Diagram
<img width="1195" height="747" alt="Screenshot 2026-02-02 085008" src="https://github.com/user-attachments/assets/a521b061-fd6d-4f25-b35d-9862c6f8339f" />

## Connection Details:

•	Input signal → Capacitor (C) → Inverting terminal (Pin 2)

•	Feedback resistor (Rf) → Between Output (Pin 6) and Pin 2

•	Non-inverting terminal (Pin 3) → Ground

•	Pin 7 → +12V

•	Pin 4 → −12V
## Theory
A Differentiator circuit produces an output voltage proportional to the rate of change of input voltage.
## Working Principle:

•	When input changes rapidly → output amplitude increases

•	When input is constant → output is zero

•	Output is inverted
## Procedure
1.	Open Proteus software.
2.	Select μA741, capacitor, resistor, signal generator, and CRO.
3.	Connect circuit in differentiator configuration.
4.	Apply ±15V power supply.
5.	Set input sine wave (1V, 1kHz).
6.	Run simulation.
7.	Observe input and output waveforms on CRO.
## Tabulation
| S.No | Input Signal        | Frequency | Expected Output (Theory)                                       | Practical Observation (Your CRO)                             |
| ---- | ------------------- | --------- | -------------------------------------------------------------- | ------------------------------------------------------------ |
| 1    | **Square wave**     | 100 Hz    | Positive spike at rising edge & negative spike at falling edge | Sharp positive and negative spikes observed at transitions   |
| 2    | **Sine wave**       | 100 Hz    | Cosine waveform (phase shifted by 90°)                         | Output sine shifted by 90° with reduced amplitude            |
| 3    | **Triangular wave** | 100 Hz    | Square wave output                                             | Nearly square waveform obtained                              |
| 4    | **Sawtooth wave**   | 100 Hz    | Constant level with sharp spike at discontinuity               | Ramp converted to constant slope output with negative spikes |

## Waveforms
•	Sine input → Cosine output (90° phase shift)
•	Square input → Positive & negative spikes
•	Triangular input → Square wave
<img width="1920" height="1200" alt="Screenshot 2026-02-02 090815" src="https://github.com/user-attachments/assets/d00a370c-f36b-4119-9457-6f0e9f2fc693" />
<img width="1920" height="1200" alt="Screenshot 2026-02-02 093144" src="https://github.com/user-attachments/assets/a61d9244-59a8-4e58-bac2-5e270ce4f3ff" />
<img width="1920" height="1200" alt="Screenshot 2026-02-02 093246" src="https://github.com/user-attachments/assets/d1c3c0a5-0d22-41fa-9427-54cf1e115926" />
<img width="1920" height="1200" alt="Screenshot 2026-02-02 093303" src="https://github.com/user-attachments/assets/94b7d4f1-7072-482b-bd14-aab6c24a1b34" />


## Result
The Differentiator circuit using μA741 Op-Amp was successfully designed and simulated in Proteus.
The output waveform is proportional to the rate of change of input voltage.
The circuit behaves as a differentiator.
## Conclusion
•	Output depends on frequency.
•	Output leads input by 90° (for sine input).
•	Higher frequency → Higher output amplitude.
•	Used in wave shaping and signal processing applications.
## Viva Questions
1.	What is a differentiator?

A differentiator is an OP-AMP circuit that produces an output voltage proportional to the rate of change (derivative) of the input signal.
 It responds strongly to rapid changes in input and weakly to slow changes.
 
2.	Write the output equation of differentiator.

<img width="218" height="77" alt="image" src="https://github.com/user-attachments/assets/d78f6172-4409-403f-9ed6-f604be4e3720" />

Where

• R → Feedback resistor

• C → Input capacitor

• Output is proportional to derivative of input and inverted

3.	Why is output leading input?

Differentiation introduces a +90° phase shift.

Since output depends on slope of input, the maximum output occurs before the input reaches its peak.
Hence, output leads input by 90° (for sinusoidal input).

4.	What happens at very high frequency?

At very high frequency:

1.Capacitive reactance becomes very small

2.Circuit gain increases significantly

3.Noise gets amplified

4.Circuit may become unstable

Therefore, ideal differentiator is not practical at high frequency.

5.	What is practical differentiator?

A practical differentiator is a modified differentiator with:

1. Input resistor (series with capacitor)

2. Feedback capacitor (parallel with resistor)

 These components:

• Limit high-frequency gain

• Reduce noise

• Improve stability

