# 📡 WNS Wireless Networks Project

## 📌 Overview
This project, developed for the **Wireless Network Systems** course, implements **Adaptive Modulation** in MATLAB/Simulink to evaluate its performance against fixed modulation schemes (**QPSK, 16-QAM, 64-QAM**) under **AWGN, Rayleigh, and Rician channel conditions**.

By dynamically adjusting the modulation scheme based on **real-time SNR estimation**, the system maintains **robustness in poor channel conditions** while **maximizing throughput in favorable conditions**.

---

## 🛠 Features
- **Turbo Encoding/Decoding** for forward error correction.
- **Adaptive Modulation Controller (AMC)** selecting modulation scheme based on measured SNR.
- **Parallel Modulator/Demodulator branches** for QPSK, 16-QAM, and 64-QAM.
- **Performance evaluation** under realistic channel models: AWGN, Rayleigh, Rician.
- **BER and PER Analysis** comparing Adaptive vs. Static schemes.
- **Constellation Diagrams** for visual insight into modulation performance.

---

## 📂 Repository Structure
├── final_plot.mlx # MATLAB Live Script for final plots
├── final_plot.pdf # Exported plots
├── static_mile3.slx # Static modulation Simulink model
├── with_encoding_mile2.slx # Adaptive modulation with Turbo encoding
├── wireless project report.pdf # Full project documentation



---

## 🔍 System Workflow
1. **Binary Data Generation** → Random binary sequence created.
2. **Turbo Encoding** → Adds forward error correction.
3. **Parallel Modulation** → Data sent to QPSK, 16-QAM, 64-QAM branches.
4. **SNR Estimation** → Measures instantaneous channel quality.
5. **Adaptive Modulation Controller** → Chooses optimal modulation index.
6. **Channel Simulation** → AWGN, Rayleigh, Rician models applied.
7. **Demodulation & Decoding** → Matches transmitter’s chosen modulation.
8. **Performance Analysis** → BER/PER metrics and visual plots.

---

## 📊 Results
- **Adaptive modulation** consistently achieved **lower BER** compared to static schemes at equivalent SNR values.
- System demonstrated **smooth switching** between modulation schemes based on channel variations.
- **Throughput improved** in good conditions without sacrificing reliability in poor conditions.

---

## 🚀 Technologies Used
- **MATLAB**
- **Simulink**
- **Digital Communication Toolboxes**

---

## 👥 Contributors
- **Ahmed Abdullah Mujtaba**
- **Basil Khowaja**

---
