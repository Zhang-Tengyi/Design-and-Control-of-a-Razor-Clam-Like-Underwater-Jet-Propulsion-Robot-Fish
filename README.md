# Design-and-Control-of-a-Razor-Clam-Like-Underwater-Jet-Propulsion-Robot-Fish
This work presents the design of a bionic jet-propelled robot inspired by the razor clam (Sinonovacula constricta), aiming to replicate its unique jet-based locomotion for underwater motion.

First, the biological structure and movement of the razor clam were analyzed. When threatened, the clam performs a rapid escape by whipping its foot and ejecting water through its siphon, reaching a speed of about 50 cm/s. High-speed imaging shows that the foot movement rotates the body by 90°, positioning the shell opening downward while the siphon—located between the foot and mantle—expels water to reduce ground friction.

Based on this mechanism, a jet-propelled robotic prototype was designed. Using SolidWorks, a magnetic drive system was created in which a motor-driven rotor with permanent magnets controls the opening and closing of the upper shell. The shell motion compresses a flexible membrane to simulate the clam’s mantle contraction and water ejection. Fluid dynamics simulations in Fluent were conducted to analyze flow characteristics, thrust, and efficiency, followed by structural optimization and prototype fabrication for testing.

A second design concept was later proposed using a tubular origami-like structure to imitate the clam’s foot contraction, generating thrust by expelling water through a nozzle. The model was also optimized and 3D printed for experimental verification.

Finally, comparative tests between the two prototypes were carried out, and the propulsion performance and movement stability were comprehensively analyzed.



# Bionic Razor-Clam-Inspired Jet-Propelled Underwater Robot

A research project exploring the **jet propulsion mechanism** of the razor clam (*Solen strictus*) to design and test a **bionic underwater robot** capable of efficient jet-based locomotion.  
Two propulsion prototypes were developed:  
1. **Magnet-Driven Shell Closure System** – simulating mantle contraction and water ejection.  
2. **Tubular Origami Structure** – imitating the clam’s foot contraction for pulsatile jet thrust.  

Both designs were modeled in **SolidWorks**, simulated in **ANSYS Fluent**, 3D printed, and experimentally tested.

---

## Table of Contents

1. [Quick Start](#quick-start)
2. [Project Overview](#project-overview)
3. [Design Structure](#design-structure)
4. [Simulation & Analysis](#simulation--analysis)
5. [Experimental Testing](#experimental-testing)
6. [Results & Discussion](#results--discussion)
7. [File Organization](#file-organization)
8. [References](#references)

---

## Quick Start

```bash
# Clone the repository
git clone https://github.com/<your-username>/bionic-razor-clam.git
cd bionic-razor-clam

# Run Fluent simulation (optional)
fluent 3ddp -i simulation/clam_jet_flow.cas
