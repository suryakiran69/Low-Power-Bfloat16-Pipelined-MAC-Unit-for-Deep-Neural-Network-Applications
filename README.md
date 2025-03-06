# Low-Power BFloat16 Pipelined MAC Unit for Deep Neural Network Applications

## Overview

This project presents the design and implementation of a **Low-Power BFloat16 Pipelined MAC (Multiply-Accumulate) Unit** for deep neural network (DNN) applications. The MAC unit is optimized for low power consumption while maintaining computational efficiency, leveraging **BFloat16 representation** to reduce memory bandwidth and improve processing speed.

### **Key Features:**
- **BFloat16 Representation**: Efficient use of reduced-precision floating-point arithmetic for DNN acceleration.
- **Pipeline Architecture**: Enhances throughput by breaking computations into multiple stages.
- **Low Power Design**: Optimized circuit-level implementations to minimize energy consumption.
- **Implemented in Cadence Virtuoso**: Circuit layout and simulation.
- **Verilog Simulation in ModelSim**: Functional verification of the design.

---

## **Block Diagram**

### **System-Level Block Diagram:**
![Block Diagram](https://raw.githubusercontent.com/suryakiran69/Low-Power-Bfloat16-Pipelined-MAC-Unit-for-Deep-Neural-Network-Applications/main/BlockDiagram.jpg)

---

## **Modules and Circuit Blocks**

### **1. Multiplication Unit**
The multiplication unit is implemented using an **8×8 multiplier** to efficiently handle BFloat16 mantissa multiplication.

- **Multiplier Circuit:**
  ![Multiplier](https://raw.githubusercontent.com/suryakiran69/Low-Power-Bfloat16-Pipelined-MAC-Unit-for-Deep-Neural-Network-Applications/main/8#%8multiplier.png)

- **Mantissa Processing Blocks:**
  - First Half: ![Mantissa First Half](https://raw.githubusercontent.com/suryakiran69/Low-Power-Bfloat16-Pipelined-MAC-Unit-for-Deep-Neural-Network-Applications/main/mantissa%20bit%20first%20half.png)
  - Second Half: ![Mantissa Second Half](https://raw.githubusercontent.com/suryakiran69/Low-Power-Bfloat16-Pipelined-MAC-Unit-for-Deep-Neural-Network-Applications/main/mantissabit%20second%20half.png)
  - Complete Mantissa Block: ![Mantissa Block](https://raw.githubusercontent.com/suryakiran69/Low-Power-Bfloat16-Pipelined-MAC-Unit-for-Deep-Neural-Network-Applications/main/mantissa%20block.png)

### **2. Accumulator Block**
- **Accumulator Design:**
  ![Accumulator](https://raw.githubusercontent.com/suryakiran69/Low-Power-Bfloat16-Pipelined-MAC-Unit-for-Deep-Neural-Network-Applications/main/accumlator%20block.png)

### **3. Exception Handling Unit**
Manages IEEE-754 BFloat16-specific conditions such as:
- **Zero Inputs Handling**
- **Infinity and NaN Detection**

- **Exponent Handling Block:**
  ![Exponent Block](https://raw.githubusercontent.com/suryakiran69/Low-Power-Bfloat16-Pipelined-MAC-Unit-for-Deep-Neural-Network-Applications/main/exponent%20block.png)

### **4. Shift Right (SHR) Block**
- **SHR Circuit Design:**
  ![SHR Block](https://raw.githubusercontent.com/suryakiran69/Low-Power-Bfloat16-Pipelined-MAC-Unit-for-Deep-Neural-Network-Applications/main/shr%20block.png)

### **5. XOR Logic & Supporting Blocks**
- **XOR Block:**
  ![XOR Block](https://raw.githubusercontent.com/suryakiran69/Low-Power-Bfloat16-Pipelined-MAC-Unit-for-Deep-Neural-Network-Applications/main/xor%20block.png)

### **6. Final Circuit Implementation**
The full circuit implementation consists of all the above modules connected appropriately to perform pipelined MAC operations.

- **Final Block Diagram:**
  ![Final Block Diagram](https://raw.githubusercontent.com/suryakiran69/Low-Power-Bfloat16-Pipelined-MAC-Unit-for-Deep-Neural-Network-Applications/main/totalfinalblockschmatic.png)

- **Layer-wise Breakdown:**
  - **First Layer:**
    ![First Layer](https://raw.githubusercontent.com/suryakiran69/Low-Power-Bfloat16-Pipelined-MAC-Unit-for-Deep-Neural-Network-Applications/main/final%20first%20layer%20blocks.png)
  - **Second Layer:**
    ![Second Layer](https://raw.githubusercontent.com/suryakiran69/Low-Power-Bfloat16-Pipelined-MAC-Unit-for-Deep-Neural-Network-Applications/main/final%20second%20half%20blocks.png)
  - **Final Check Symbol Block:**
    ![Final Check Symbol](https://raw.githubusercontent.com/suryakiran69/Low-Power-Bfloat16-Pipelined-MAC-Unit-for-Deep-Neural-Network-Applications/main/final%20block%20check%20symbol.png)

---

## **Implementation Details**
### **Tools Used:**
- **Cadence Virtuoso**: CMOS circuit layout and simulations.
- **ModelSim**: Verilog-based functional verification.
- **GitHub**: Version control and project management.

### **Simulation and Testing**
- The design was tested with multiple floating-point inputs to verify correctness.
- Power analysis was conducted to ensure the low-power objective was met.

---

## **How to Run the Project**
1. Clone the repository:
   ```sh
   git clone https://github.com/suryakiran69/Low-Power-Bfloat16-Pipelined-MAC-Unit-for-Deep-Neural-Network-Applications.git
2. Open the Verilog files in ModelSim for simulation.
3. Open the Cadence Virtuoso files to analyze the circuit layout.
4. Review the included images for detailed circuit diagrams.
## **Future Enhancements**

    - Optimization for higher clock frequencies.
    - FPGA implementation for real-time applications.
    - Integration with AI accelerators for faster inference in deep learning models.
## **Contributors**

👨‍💻 Naralasetti Umesh Surya Kiran
📧  ![LinkedIn]([https://www.linkedin.com/in/n-u-surya-kiran/])

## **License**

This project is licensed under the MIT License. Feel free to use and modify the code as needed.

**Thank you for exploring this project! 🚀**
