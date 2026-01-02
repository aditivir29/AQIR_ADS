# Quantum Image Representation Evaluation

This project demonstrates a **step-by-step workflow** to study how images can be stored and processed using **quantum computing simulations**.  
We compare two quantum image representation methods and analyze their efficiency using simulation-based metrics.

The entire workflow follows **7 clear steps**, from image upload to result visualization.

---

## Project Workflow (7 Steps)

---

### **Step 1: Upload / Load Image**

- An image is taken from a dataset (for example, Chest X-Ray images from Kaggle)
- The image can also be uploaded by the user
- At this stage, the image is a normal digital image stored on a classical computer

**Tools Used:**
- Python
- OpenCV
- PIL (Python Imaging Library)

---

### **Step 2: Resize and Normalize Image**

- The image size is reduced (for example, to 32×32 pixels)
- Pixel values are normalized to a small range
- This is required because current quantum systems cannot handle large images

**Tools Used:**
- NumPy
- OpenCV
- Scikit-Image

---

### **Step 3: Choose Quantum Image Representation**

- Two quantum image representation methods are selected:
  - NEQR (stores pixel position and brightness exactly)
  - Hybrid Quantum Image Representation (uses fewer quantum resources)
- Both methods are applied to the same image for fair comparison

**Tools Used:**
- Python functions

---

### **Step 4: Quantum Encoding Using Simulator**

- The image is converted into quantum bits (qubits)
- A quantum circuit is created to represent the image
- The process runs on a **quantum simulator**, not real hardware

**Tools Used:**
- Azure Quantum Development Kit
- Q# (Quantum programming language)
- Quantum Simulator

---

### **Step 5: Extract Quantum Resource Metrics**

- The simulator reports how many resources are required:
  - Number of qubits
  - Number of quantum gates
  - Estimated circuit complexity
- These values help determine which method is more efficient

**Tools Used:**
- Azure Resource Estimator
- Pandas

---

### **Step 6: Reconstruct the Image**

- The quantum-encoded image is converted back into a classical image
- The reconstructed image is compared with the original image
- This checks whether the image was stored correctly

**Tools Used:**
- Q#
- NumPy
- Matplotlib

---

### **Step 7: Visualization and Comparison Dashboard**

- Results are shown using graphs and images
- Side-by-side comparison of:
  - Original image
  - Reconstructed images
  - Resource usage for each method

**Tools Used:**
- Streamlit
- Plotly
- Pandas

---

## 📂 Project Structure

