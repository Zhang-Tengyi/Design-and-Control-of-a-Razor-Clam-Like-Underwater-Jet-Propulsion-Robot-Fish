# Design-and-Control-of-a-Razor-Clam-Like-Underwater-Jet-Propulsion-Robot-Fish
This work presents the design of a bionic jet-propelled robot inspired by the razor clam (Sinonovacula constricta), aiming to replicate its unique jet-based locomotion for underwater motion.

First, the biological structure and movement of the razor clam were analyzed. When threatened, the clam performs a rapid escape by whipping its foot and ejecting water through its siphon, reaching a speed of about 50 cm/s. High-speed imaging shows that the foot movement rotates the body by 90°, positioning the shell opening downward while the siphon—located between the foot and mantle—expels water to reduce ground friction.

Based on this mechanism, a jet-propelled robotic prototype was designed. Using SolidWorks, a magnetic drive system was created in which a motor-driven rotor with permanent magnets controls the opening and closing of the upper shell. The shell motion compresses a flexible membrane to simulate the clam’s mantle contraction and water ejection. Fluid dynamics simulations in Fluent were conducted to analyze flow characteristics, thrust, and efficiency, followed by structural optimization and prototype fabrication for testing.

A second design concept was later proposed using a tubular origami-like structure to imitate the clam’s foot contraction, generating thrust by expelling water through a nozzle. The model was also optimized and 3D printed for experimental verification.

Finally, comparative tests between the two prototypes were carried out, and the propulsion performance and movement stability were comprehensively analyzed.



# Bionic Razor-Clam-Inspired Jet-Propelled Underwater Robot  

A research project exploring **jet propulsion in bionic underwater robots**, inspired by the *razor clam (Solen strictus)*.  
Two different propulsion mechanisms were designed, simulated, and tested to study **bio-inspired jet locomotion** and its efficiency in underwater movement.  

---

## Table of Contents
1. [Project Overview](#project-overview)  
2. [Bio-Inspiration & Motivation](#bio-inspiration--motivation)  
3. [Design Concepts](#design-concepts)  
4. [Simulation & Analysis](#simulation--analysis)  
5. [Experimental Testing](#experimental-testing)  
6. [Results & Discussion](#results--discussion)  
7. [Folder Structure](#folder-structure)  
8. [Future Work](#future-work)  
9. [References](#references)  
10. [Acknowledgements](#acknowledgements)  

---

## 🧠 Project Overview  

This repository accompanies the research *“Design and Control of a Razor-Clam-Inspired Jet-Propelled Robotic Fish.”*  
The goal is to replicate the razor clam’s unique **foot whipping and water-jet propulsion** mechanism, which allows rapid escape movement (~50 cm/s).  

The project combines:  
- **Mechanical Design** in SolidWorks  
- **CFD Simulation** in ANSYS Fluent  
- **Control Circuit Design** using C51 MCU  
- **3D Printing & Experimental Testing**  

---

## 🌊 Bio-Inspiration & Motivation  

Razor clams exhibit a **composite propulsion** combining:  
1. **Foot whipping** — rotates the body 90° about the longitudinal axis  
2. **Jet ejection** — mantle contraction expels stored water through the siphon  

This efficient escape mechanism inspired the development of a **bionic jet-propelled robot** that mimics the clam’s dual action for underwater locomotion.

*Example schematic of the clam motion:*  
![Bio-inspired diagram](figures/bio_inspiration.png)  

---

## 🧩 Design Concepts

### Ⅰ. Shell-Closure Jet Propulsion System (上下壳闭合式)

This design mimics the **mantle contraction** of the razor clam.  
A pair of permanent magnets mounted on the upper shell and motor rotor alternate between attraction and repulsion to open and close the shell.

- **Structure:** upper & lower shells + flexible sealing film  
- **Drive:** DC motor → rotor → magnetic actuation  
- **Function:** cyclic compression of the internal water chamber to generate jet thrust  
- **Control:** STC89C52RC microcontroller + Bluetooth module  
- **Simulated speed:** ≈ 19 mm/s  

![Shell structure](figures/shell_design.png)

---

### Ⅱ. Tubular Origami Jet Propulsion System (管状折纸结构式)

The second design imitates the **foot contraction** of the razor clam using a **tubular origami mechanism** with spring energy storage.  
A gear-rack system driven by an N20 motor compresses the origami structure to expel water and generate thrust.

- **Structure:** origami tube + spring + gear-rack linkage  
- **Drive:** motor → half gear → linkage → spring compression  
- **Function:** pulse-type jet propulsion with larger water-volume change  
- **Performance:** faster (≈ 28 mm/s), more stable than shell type  

![Origami structure](figures/origami_design.png)

---

## 💻 Simulation & Analysis  

CFD simulations were performed using **ANSYS Fluent**.  
Key parameters analyzed:  
- Jet thrust \( F = \dot{m} v_e \)  
- Propulsion efficiency \( \eta = \frac{2U}{v_e + U} \)  
- Pressure and velocity distribution  
- Flow resistance vs nozzle geometry  

*Example Fluent results:*  
![CFD contours](figures/fluent_results.png)

**Predicted performance:**  
| Model | Predicted Speed | Notes |
| ------ | ---------------- | ----- |
| Magnet-driven shell | 1.8 cm/s | Stable but low thrust |
| Origami structure | 2.8 cm/s | Stronger impulse, higher efficiency |

---

## 🧪 Experimental Testing  

**Setup:**  
- Water tank (100 cm × 30 cm × 30 cm)  
- STC89C52RC microcontroller + Bluetooth control  
- N20 reduction motor for actuation  

*Testing snapshot:*  
![Experiment photo](figures/experiment.png)

**Results summary:**  

| Motor Speed (r/min) | Avg. Velocity (mm/s) |
| -------------------- | -------------------- |
| 30 | 4.0 |
| 60 | **19.3** |
| 90 | 12.4 |

---

## 📊 Results & Discussion  

- The **magnet-driven design** confirmed feasibility of jet propulsion, though efficiency remained moderate.  
- The **origami-based system** achieved higher propulsion speed and smoother jet pulses.  
- **Optimizing nozzle area** and **membrane elasticity** significantly enhanced thrust.  
- Future improvements may include **miniaturized waterproof electronics** and **adjustable directional control**.  

---

## 📁 Folder Structure  


