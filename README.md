# ME 4351 Control Systems

Interactive tools for ME 4351 Control Systems, Texas State University, Fall 2026.

## PID Tuning Lab

[`pid-tuning-lab/index.html`](pid-tuning-lab/index.html) is a single HTML file with no dependencies. Open it in any browser, or use the GitHub Pages link.

- Sliders for K<sub>p</sub>, K<sub>i</sub>, K<sub>d</sub> with live closed-loop step response
- Overshoot, 2% settling time, 10–90% rise time and steady-state error
- Closed-loop poles on the s-plane, with plant poles and controller zeros
- Pin a response to compare before and after
- Plants: 1/[(s+1)(s+2)(s+3)], robot joint 1/[s(s+2)], tank level 2/(5s+1)
- Presets from lecture: P, PI, PID, Ziegler–Nichols (ultimate gain and reaction curve), fine-tuned

How it works: the controller G<sub>c</sub>(s) = (K<sub>d</sub>s² + K<sub>p</sub>s + K<sub>i</sub>)/s and plant are combined into the closed-loop transfer function T(s) = G<sub>c</sub>G / (1 + G<sub>c</sub>G), realized in controllable canonical form and simulated with 4th-order Runge–Kutta. Poles come from the Durand–Kerner root finder.
