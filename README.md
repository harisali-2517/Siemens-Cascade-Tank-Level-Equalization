# Cascade Tank Level Equalization Control

A dual-tank fluid balancing architecture programmed on a **Siemens S7-1200 (CPU 1215C)** using **TIA Portal**. 

### 🌊 Project Highlights
* **Analog Scaling & Delta Math:** Scaled raw level sensor inputs for two independent tanks (0-100%). Utilized arithmetic blocks (`SUB`, `ABS`) to continuously calculate the absolute absolute level difference between Tank A and Tank B.
* **Automated Balancing:** Configured comparator networks to automatically actuate a transfer pump whenever the fluid discrepancy between the two tanks exceeded a 20% threshold.
* **Anti-Short-Cycling Logic:** Engineered a 10-second `TON` (Start-Delay Timer) on the transfer pump logic to prevent rapid mechanical cycling and "chasing" caused by minor surface fluid fluctuations or sensor noise.

### 📂 Repository Files
* **Ladder_Logic.pdf:** PDF export of the Main OB1 ladder logic and arithmetic blocks.
* **Cascade_Equalization_Archive.zap15:** Raw TIA Portal V15 archive file.
