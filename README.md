# Design-and-Control-of-a-Razor-Clam-Like-Underwater-Jet-Propulsion-Robot-Fish
This work presents the design of a bionic jet-propelled robot inspired by the razor clam (Sinonovacula constricta), aiming to replicate its unique jet-based locomotion for underwater motion.

First, the biological structure and movement of the razor clam were analyzed. When threatened, the clam performs a rapid escape by whipping its foot and ejecting water through its siphon, reaching a speed of about 50 cm/s. High-speed imaging shows that the foot movement rotates the body by 90°, positioning the shell opening downward while the siphon—located between the foot and mantle—expels water to reduce ground friction.

Based on this mechanism, a jet-propelled robotic prototype was designed. Using SolidWorks, a magnetic drive system was created in which a motor-driven rotor with permanent magnets controls the opening and closing of the upper shell. The shell motion compresses a flexible membrane to simulate the clam’s mantle contraction and water ejection. Fluid dynamics simulations in Fluent were conducted to analyze flow characteristics, thrust, and efficiency, followed by structural optimization and prototype fabrication for testing.

A second design concept was later proposed using a tubular origami-like structure to imitate the clam’s foot contraction, generating thrust by expelling water through a nozzle. The model was also optimized and 3D printed for experimental verification.

Finally, comparative tests between the two prototypes were carried out, and the propulsion performance and movement stability were comprehensively analyzed.



A research project exploring the jet-propulsion mechanism of the razor clam (Solen strictus) to design and test a bionic underwater robot capable of jet-based locomotion.
Two propulsion schemes are implemented:

Magnet-Driven Shell Closure System – simulating mantle contraction and water ejection.

Tubular Origami Structure – imitating foot contraction for pulsatile jet thrust.

Both prototypes were modeled in SolidWorks, analyzed in Fluent, 3D-printed, and experimentally tested in water tanks.

Table of Contents

Quick Start

Project Overview

Design Structure

Simulation & Analysis

Experimental Testing

Results & Discussion

File Organization

References

Quick Start
# Clone the repository
$ git clone https://github.com/<your-org>/bionic-razor-clam.git
$ cd bionic-razor-clam

# CAD & Simulation
# Models built with SolidWorks 2023 and simulated using ANSYS Fluent

# Optional: run Fluent case file
$ fluent 3ddp -i /sim/clam_jet_flow.cas


After simulation, plots of velocity field, pressure distribution, and drag–thrust curves appear in the /results/ folder.

Project Overview

This work investigates jet propulsion in benthic shellfish and translates biological principles into robotic design.
The razor clam moves by foot whipping and water ejection, reaching ~0.5 m/s during escape.
High-speed video analysis revealed a 90° axial rotation that aligns the siphon downward to minimize drag.

Design Structure

Two main propulsion prototypes were developed:

1. Magnet-Driven Shell Closure

A motor-rotor system with paired permanent magnets drives shell opening/closing.

A flexible membrane seals upper and lower shells to mimic mantle contraction.

Controlled by a C51 microcontroller + Bluetooth module for remote testing.

2. Tubular Origami Structure

Inspired by the clam’s foot contraction, using spring-assisted origami tubes.

A gear-rack system converts motor rotation into axial compression.

Generates strong pulsatile jets for efficient thrust.

Simulation & Analysis

Fluent CFD simulations calculate jet thrust, flow distribution, and hydrodynamic resistance.

Jet thrust 
𝐹
=
𝑚
˙
𝑣
𝑒
F=
m
˙
v
e
	​

, efficiency 
𝜂
=
2
𝑈
𝑣
𝑒
+
𝑈
η=
v
e
	​

+U
2U
	​

.

Results show optimized shell curvature and nozzle area significantly improve efficiency.

Predicted velocity ≈ 1.8 cm/s (steady motion phase).

Experimental Testing

Prototypes tested in a 1 m × 0.3 m × 0.3 m water tank.

Video-tracked to measure displacement and velocity.

Performance metrics:

Motor Speed (r/min)	Avg. Velocity (mm/s)
30	4.0
60	19.3
90	12.4
Results & Discussion

The magnet-driven model validated periodic jet propulsion, though with moderate thrust.

The origami model achieved higher impulse efficiency and stability (max ≈ 28 mm/s).

Future improvements: miniaturized electronics, soft actuators, and adjustable nozzle control.

File Organization
bionic-razor-clam/
│
├── /cad_models/             # SolidWorks part & assembly files
├── /simulation/             # Fluent .cas / .dat files
├── /control/                # STM/C51 MCU control code
├── /results/                # CFD plots & experimental data
├── /docs/
│   ├── thesis.pdf
│   └── figures/
└── README.md
