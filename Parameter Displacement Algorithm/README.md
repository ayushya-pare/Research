
## Inverse Parameter Displacement SGD Optimizer

A new adaptive Stochastic Gradient Descent (SGD) algorithm that dynamically adjusts the learning rate for each model parameter based on the displacement of the parameter values across iterations. The approach enhances convergence and model accuracy, outperforming traditional optimizers like SGD with momentum and Adam.

### **Algorithm**

- **Inverse Model-Parameter Difference SGD**:
  - Computes adaptive learning rates inversely proportional to the displacement of model parameters from preceding iterations.
  - Reduces the learning rate for parameters with large displacements (steeper gradients) and increases it for small displacements (flatter gradients).
  - The adaptive update rule:
    \[
    \theta_{k+1} = \theta_k - \eta_k g(\theta_k, \xi) + \beta (\theta_k - \theta_{k-1})
    \]
    where \(\eta_k\) is the adaptive learning rate.

---

### **Tools / Technologies Used**

- **Framework**: TensorFlow  
- **Datasets**: CIFAR-10, CIFAR-100, ImageNet  
- **Optimizers**: SGD with momentum, Adam, AdaBelief, LookAhead, AdamW  

---

### **Results**

- **Performance Improvements**:
  - **ImageNet**: 3.85% accuracy improvement over SGD with momentum and 1.23% over Adam.
  - **CIFAR-10 / CIFAR-100**: The proposed algorithm achieved faster convergence and higher accuracy compared to other state-of-the-art optimizers.

This algorithm shows superior convergence efficiency by dynamically adjusting learning rates based on parameter displacements, making it robust across various datasets and architectures.
