
🚀 **Envelope-LMS Multipath Suppression**:  
An adaptive algorithm to suppress **Multipath Interference (MpI)** in **Time-of-Flight (ToF)** cameras by leveraging the amplitude envelope of the transmitted signal. The method uses an adaptive Least Mean Squares (LMS) filter to minimize deviations caused by MpI, improving the accuracy of depth measurements significantly.

---

### **Algorithm*

- **Envelope-LMS Algorithm**:
  - Exploits the fact that the amplitude envelope of a sinusoidal signal remains constant unless corrupted by MpI.
  - Uses an LMS adaptive filter to minimize deviations between the received signal's envelope and the expected constant envelope.
  - Iteratively updates filter weights to suppress MpI, thereby correcting the depth measurement errors.

---

### **Tools / Technologies Used**

- **Software**: MATLAB  
- **Hardware**: ToF camera setup with laser diodes and photodetectors  
- **Adaptive Filtering**: Least Mean Squares (LMS) algorithm, IIR filters  

---

### **Results**

- **Simulation**: Achieved depth correction within 0.001 m accuracy under multiple MpI scenarios.  
- **Experiments**:  
  - Improved depth measurements for objects like a pencil, metal wire, and eraser by mitigating MpI.  
  - Corrected depth errors even when objects moved or the scene changed abruptly.  

- **Key Improvement**: Outperformed existing MpI suppression techniques without additional hardware requirements or assumptions about light properties.