
# 🔍 Adulteration Detection in Spices  
**Detecting Papaya Seed Adulteration in Black Pepper Using YOLOv8s**

![Pepper vs Papaya Example](https://via.placeholder.com/800x200?text=Adulteration+Detection+in+Spices)

## 📌 Overview

This project addresses the critical issue of **food adulteration in spices**, focusing on the **detection of papaya seed adulteration in black pepper** using deep learning and computer vision. Leveraging the **YOLOv8s** object detection architecture, we trained a model to identify and quantify adulteration from high-resolution images, providing a **fast, automated, and non-destructive solution** for spice quality assurance.

---

## 📂 Project Structure

- `data/`: Collected and organized image dataset (pure, adulterated samples)
- `labels/`: YOLOv8 annotation files
- `models/`: Training scripts and model checkpoints
- `notebooks/`: Jupyter/Colab notebooks for experimentation
- `results/`: Evaluation plots and detection outputs
- `README.md`: Project documentation

---

## 🧪 Objective

To build a **real-time machine learning-based system** to:
- Detect individual **black pepper and papaya seeds**
- Classify them into respective categories
- **Estimate the degree of adulteration** in spice samples

---

## 📸 Dataset

We constructed a custom dataset containing 1,277 high-resolution RGB images:
- **552 images** of pure black pepper
- **425 images** of pure papaya seeds
- **300 images** of adulterated samples

### Adulteration Simulation:
- Created **63 variations** of adulterated mixtures with 10 sample images each
- Varying seed ratios: 10%, 20%, … up to 80% papaya seed presence
- Captured using **iPhone 16 (48MP Fusion Camera)** under controlled lighting on a white background

Annotation was done using [Label Studio](https://github.com/heartexlabs/label-studio) and follows YOLOv8 format.

---

## 🧠 Model Architecture

We used **YOLOv8s**, a lightweight real-time object detection model by Ultralytics.

### Key Components:
- **Backbone**: CSPDarknet with FPN for multi-scale detection
- **Input Resolution**: 640×640
- **Optimizer**: SGD + Momentum
- **Data Augmentation**: Mosaic, flipping, rotation, brightness tuning
- **Training Platform**: Google Colab with NVIDIA Tesla T4 GPU

---

## 📈 Results

### Evaluation Metrics:
| Metric                        | Value       |
|------------------------------|-------------|
| Mean Seed Detection Accuracy | **88.99%**  |
| Mean Relative Adulteration Error (MRAE) | **12.27%** |
| Normalized RMSE              | **0.0813**  |

### Visual Outputs:
- Side-by-side comparisons of **predicted vs actual seed counts**
- Predicted **adulteration percentages** matching true labels
- Bounding boxes with class labels on seed instances

---

## 🔍 Model Capabilities

- **Accurate detection** even in dense or sparse seed distributions
- Effective at **quantifying adulteration**
- High-speed inference suitable for **real-time industrial applications**

---

## 🚀 Future Work

- Use of **hyperspectral imaging** for chemical-level detection
- Enhanced models with **larger annotated datasets**
- On-device deployment for **edge computing** and **industry adoption**

---

## 🙏 Acknowledgments

We thank the **Department of Computer Science & Engineering** at **IIT Ropar** for providing the infrastructure and guidance. Special thanks to our faculty advisor for their continuous support.

---

## 👥 Authors

- [Priyanshu Shukla](mailto:2024csm1016@iitrpr.ac.in)
- [Naveen Kamalla](mailto:2024csm1009@iitrpr.ac.in)
- [Jugal Alan](mailto:2024aim1004@iitrpr.ac.in)

---

## 📄 License

This project is for academic and research purposes. Please contact the authors for commercial use or collaboration.
