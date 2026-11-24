

# Radio Tuning Using an RLC Circuit

### How Does a Radio Pick One Station Out of Hundreds?

**Modeling Radio Frequency Selection Using Second-Order Differential Equations**

## Project Overview

When we turn on an FM radio, many stations broadcast signals simultaneously. However, by adjusting the tuning dial, we can select one station without hearing all the others.

For example, a radio tuned to **100.0 MHz** should respond strongly to that frequency while reducing interference from nearby stations operating at **98.5 MHz** and **101.5 MHz**.

But how does a radio distinguish between these frequencies?

This project explores how an **RLC (Resistor-Inductor-Capacitor) circuit** uses electrical resonance to respond selectively to different radio frequencies.

Using **second-order differential equations and SageMath**, we will model the circuit's behavior, investigate its frequency response, and analyze how changing resistance and capacitance affects radio tuning.

## Project Objectives

The main objectives of this project are to:

- Understand the role of resonance in radio frequency selection.
- Derive a second-order differential equation for a series RLC circuit.
- Calculate the capacitance required to tune a circuit to 100 MHz.
- Use SageMath to solve the differential equation numerically.
- Visualize circuit current as a function of time.
- Compare responses at different incoming signal frequencies.
- Investigate how resistance affects frequency selectivity.

## Problem Statement

Radio receivers are exposed to multiple signals operating at different frequencies. A tuning circuit must respond strongly to a desired frequency while reducing the response to unwanted frequencies.

This project investigates how an RLC circuit achieves frequency selectivity through resonance and how changes in circuit parameters influence its performance.

## Mathematical Model

We use a simplified series RLC circuit governed by Kirchhoff's Voltage Law.

[Download the LRC circuit PDF](lrc-circuit.pdf)

The differential equation is:

$$
L\frac{d^2q}{dt^2}+R\frac{dq}{dt}+\frac{1}{C}q=E(t)
$$

Where:

- **L** = Inductance (H)
- **R** = Resistance (Ω)
- **C** = Capacitance (F)
- **q(t)** = Capacitor charge (C)
- **E(t)** = Applied voltage (V)
- **t** = Time (s)

The incoming radio signal is modeled as a sinusoidal voltage:

$$
E(t)=E_0\cos(2\pi ft)
$$

Combining both equations gives:

$$
\boxed{Lq''+Rq'+\frac{1}{C}q=E_0\cos(2\pi ft)}
$$

This second-order differential equation allows us to study how the circuit responds to signals of different frequencies.

### Circuit Parameters

The following hypothetical values are used:

| Parameter | Value |
|---|---|
| Inductance (L) | 100 nH |
| Resistance (R) | 10 Ω |
| Input voltage amplitude (E₀) | 1 V |
| Desired frequency (f) | 100 MHz |
| Initial capacitor charge, q(0) | 0 C |
| Initial current, q'(0) | 0 A |

The required capacitance is calculated using the resonant frequency relationship:

$$
f_0=\frac{1}{2\pi\sqrt{LC}}
$$

Rearranging:

$$
C=\frac{1}{4\pi^2f_0^2L}
$$

For a desired resonant frequency of 100 MHz and an inductance of 100 nH:

$$
C\approx25.33\text{ pF}
$$

### Model Assumptions

- The resistor, inductor, and capacitor behave as ideal, linear circuit components.
- Circuit parameters remain constant during each simulation.
- Incoming radio signals are represented by sinusoidal voltage sources.
- The capacitor is initially uncharged.
- No current flows when the simulation begins.
- The circuit represents only the frequency-selection stage, not a complete radio receiver.

## Research Questions

This project aims to answer three main questions:

1. What capacitance is required for an RLC circuit with an inductance of 100 nH to resonate at 100 MHz?
2. How does the circuit's response change when the incoming signal operates at 98.5 MHz or 101.5 MHz instead of 100 MHz?
3. How does changing resistance affect the circuit's ability to distinguish between nearby frequencies?

## Hypothesis

We predict that the circuit will produce its largest steady-state current response when the incoming signal matches its resonant frequency.

Increasing resistance is expected to reduce the peak current response and make the circuit less selective between nearby frequencies.

## Numerical Simulation Using SageMath

SageMath will be used to:

1. Solve the second-order differential equation with the specified initial conditions.
2. Plot the current as a function of time.
3. Analyze the circuit's response at different frequencies.
4. Compare frequency-response curves for different resistance values.
5. Interpret the mathematical results in the context of real-world radio tuning.

## Expected Results

The simulations are expected to demonstrate that:

- The strongest steady-state current response occurs at resonance.
- Signals operating away from the resonant frequency produce smaller responses.
- Changing capacitance shifts the resonant frequency.
- Increasing resistance reduces the peak response and broadens the resonance curve.

These observations will help explain how electrical resonance contributes to frequency selection in radio receivers.

## Tools and Technologies

- **SageMath** — Differential equation solving, numerical simulations, and graphing.
- **Python** — Supporting mathematical computations within SageMath.
- **GitHub** — Project documentation, version control, and code organization.
- **LaTeX** — Mathematical equations and documentation.

## Real-World Applications

The principles explored in this project are relevant to:

- AM and FM radio receivers
- Frequency-selective filters
- Wireless communication systems
- Resonant electrical circuits
- Signal processing and electronic circuit design

## References

Relevant references will include physics resources covering RLC circuits, electrical resonance, second-order differential equations, and official SageMath documentation.
