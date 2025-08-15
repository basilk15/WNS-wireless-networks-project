# 📡Adaptive Modulation in AWGN, Rayleigh and Rician Channels Under Realistic Propagation Effects: MATLAB-Based KPI Analysis

> **A comprehensive MATLAB/Simulink implementation comparing adaptive modulation against fixed-modulation schemes under realistic propagation conditions.**

## 🎯 Project Overview

This project demonstrates the superior performance of **Adaptive Modulation and Coding (AMC)** systems over traditional fixed-modulation schemes in wireless communication channels. Our implementation dynamically switches between QPSK, 16-QAM, and 64-QAM based on real-time channel conditions.

### 👥 Team Members
- **Ahmed Abdullah Mujtaba**
- **Basil Khowaja**

## 🚀 Key Features

- **Real-time SNR Estimation** - Continuous channel quality monitoring
- **Dynamic Modulation Switching** - Intelligent selection between QPSK, 16-QAM, and 64-QAM
- **Forward Error Correction** - Turbo coding for enhanced reliability
- **Performance Analysis** - Comprehensive BER comparison across different channel models
- **Realistic Channel Models** - AWGN, Rayleigh, and Rician fading channels

## 🏗️ System Architecture

```
📊 Binary Data Generation
    ↓
🔒 Turbo Encoder (FEC)
    ↓
🔀 Three Parallel Branches:
    ├── QPSK Modulator
    ├── 16-QAM Modulator
    └── 64-QAM Modulator
    ↓
📡 AMC Controller (SNR-based switching)
    ↓
🌊 Channel (AWGN/Rayleigh/Rician)
    ↓
📨 Receiver with parallel demodulators
    ↓
🔓 Turbo Decoder
    ↓
📈 Performance Analysis
```

## 💡 How It Works

1. **Encoding**: Random binary sequences are processed through Turbo encoding for error correction
2. **Modulation**: Three parallel modulation schemes generate complex baseband waveforms
3. **Adaptive Control**: Real-time SNR estimator feeds an AMC controller that maps channel quality to modulation index
4. **Channel Transmission**: Selected waveform passes through realistic propagation channels
5. **Reception**: Parallel demodulators process the received signal, with AMC controller selecting the appropriate output
6. **Performance Evaluation**: System automatically adapts to maintain optimal balance between robustness and throughput

## 📊 Performance Results

Our simulations demonstrate that **adaptive modulation significantly outperforms static schemes**:

- ✅ **Lower BER** at equivalent SNR levels
- ✅ **Enhanced throughput** in favorable channel conditions  
- ✅ **Maintained robustness** during channel degradation
- ✅ **Seamless adaptation** to varying propagation effects

## 📁 Repository Structure

```
WNS-wireless-networks-project/
├── 📄 final_plot.mlx          # Main analysis script
├── 📄 final_plot.pdf          # Results visualization
├── 📊 static_mile3.slx        # Static modulation comparison
├── 📊 with_encoding_mile2.slx # Adaptive system with encoding
├── 📋 wireless project report.pdf # Comprehensive project report
└── 📖 README.md              # This file
```

## 🛠️ Requirements

- **MATLAB** R2020a or later
- **Simulink** 
- **Communications Toolbox**
- **Signal Processing Toolbox**

## 🚀 Getting Started

1. **Clone the repository**
   ```bash
   git clone https://github.com/basilk15/WNS-wireless-networks-project.git
   cd WNS-wireless-networks-project
   ```

2. **Open MATLAB** and navigate to the project directory

3. **Run the simulation**
   - Open `final_plot.mlx` for performance analysis
   - Load `with_encoding_mile2.slx` for the main adaptive system
   - Compare with `static_mile3.slx` for baseline performance

4. **View results** in the generated plots and constellation diagrams

## 📈 Key Performance Indicators (KPIs)

Our analysis focuses on:
- **Bit Error Rate (BER)** across SNR ranges
- **Packet Error Rate** monitoring
- **Constellation quality** visualization
- **Throughput optimization** metrics
- **Channel adaptation** responsiveness

## 🔬 Technical Implementation

### AMC Controller Logic
```matlab
function modulation_index = amc_controller(snr_estimate)
    if snr_estimate < threshold_1
        modulation_index = 1;    % QPSK
    elseif snr_estimate < threshold_2
        modulation_index = 2;    % 16-QAM
    else
        modulation_index = 3;    % 64-QAM
    end
end
```

### Channel Models Tested
- **AWGN**: Additive White Gaussian Noise
- **Rayleigh**: Non-line-of-sight fading
- **Rician**: Line-of-sight with multipath components

## 📚 Academic Context

This project was developed as part of the **Wireless Network Systems** course, demonstrating practical implementation of adaptive communication techniques used in modern wireless standards like LTE and 5G.

## 🎓 Learning Outcomes

- Understanding of adaptive modulation principles
- Hands-on experience with MATLAB/Simulink for communications
- Analysis of realistic channel propagation effects
- Performance optimization in wireless systems
- Implementation of forward error correction techniques


**⭐ Star this repository if you found it helpful for your wireless communications studies!**
