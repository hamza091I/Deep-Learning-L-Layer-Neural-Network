Deep Neural Network from Scratch (L-Layer Architecture)

A modular, highly-optimized implementation of a deep L-layer Neural Network built completely from scratch using **Python** and **NumPy**. This repository demonstrates the mathematical foundations of deep learning without relying on high-level frameworks like TensorFlow or PyTorch.

---

## Key Features

* **Pure NumPy Implementation:** Core mathematical operations vectorized for fast performance.
* **Flexible Layer Scaling:** Dynamic $L$-layer architecture supporting custom layer dimensions.
* **Activation Functions:** Custom implementations of `ReLU` and `Sigmoid` with their exact mathematical derivatives.
* **Complete Backpropagation Pipeline:** Manual derivation and computation of gradients ($\frac{\partial J}{\partial W}$, $\frac{\partial J}{\partial b}$, and $\frac{\partial J}{\partial A}$).
* **Optimization:** Standard Gradient Descent with He-style parameter initialization.
* **Self-Contained Data Pipeline:** Built-in synthetic dataset generator for instant unit testing and training verification.

---

##  Network Architecture & Flow

The network implements the following pipeline:

1. **Forward Propagation:** 
   $$\text{[LINEAR} \rightarrow \text{RELU]}^{(L-1)} \rightarrow \text{[LINEAR} \rightarrow \text{SIGMOID]}$$
2. **Loss Computation:** Binary Cross-Entropy Cost Function.
3. **Backward Propagation:** Chain rule gradient calculation moving backwards through the layers.
4. **Parameter Updates:** Gradient Descent optimization step.

---

##  Code Structure (Cell Breakdown)

The codebase is organized into **10 modular cells** for clarity and scannability:

| Cell | Module Description |
| :--- | :--- |
| **Cell 1** | Activation functions (`sigmoid`, `relu`) & derivatives |
| **Cell 2** | Synthetic binary dataset generator |
| **Cell 3** | Shallow (2-Layer) parameter initialization |
| **Cell 4** | Deep ($L$-Layer) He-style parameter initialization |
| **Cell 5** | Linear forward step ($Z = W \cdot A + b$) |
| **Cell 6** | Combined Linear $\rightarrow$ Activation forward step |
| **Cell 7** | Full $L$-Layer forward propagation model |
| **Cell 8** | Binary Cross-Entropy cost calculation |
| **Cell 9** | Comprehensive $L$-Layer backward propagation |
| **Cell 10** | Gradient Descent parameter update & training loop |
