# 🧠 Custom CNN for Traffic Sign Classification

This project implements a **Custom Convolutional Neural Network (CNN)** to classify traffic signs using TensorFlow and Keras.  
It is designed to process 64×64 RGB images and predict among **43 different traffic sign classes** (as in the [German Traffic Sign Recognition Benchmark (GTSRB)](https://benchmark.ini.rub.de/gtsrb_news.html)).

---

## 🧩 Model Architecture

The following CNN architecture was built and trained for the classification task:

![Custom CNN Architecture](Custom_CNN.png)

| Layer Type | Output Shape | Parameters | Description |
|-------------|--------------|-------------|--------------|
| Input | (64, 64, 3) | 0 | Input RGB images |
| Data Augmentation | (64, 64, 3) | 0 | Random transformations (flip, rotation, zoom) |
| Conv2D | (64, 64, 32) | 896 | 3×3 filters, ReLU activation |
| Batch Normalization | (64, 64, 32) | 128 | Normalize activations |
| MaxPooling2D | (32, 32, 32) | 0 | 2×2 pooling |
| Conv2D | (32, 32, 64) | 18,496 | Deeper feature extraction |
| Batch Normalization | (32, 32, 64) | 256 | Normalize activations |
| MaxPooling2D | (16, 16, 64) | 0 | 2×2 pooling |
| Conv2D | (16, 16, 128) | 73,856 | More complex feature maps |
| Batch Normalization | (16, 16, 128) | 512 | Normalize activations |
| MaxPooling2D | (8, 8, 128) | 0 | Downsampling |
| Flatten | (8192) | 0 | Flatten to vector |
| Dense | (256) | 2,097,408 | Fully connected layer |
| Dropout | (256) | 0 | Regularization |
| Dense | (43) | 11,051 | Softmax output for 43 classes |

**Total Parameters:** 2,202,603  
**Trainable Parameters:** 2,202,155  
**Non-trainable Parameters:** 448

---

## 🚀 Features

- Custom CNN designed from scratch for traffic sign recognition.  
- Includes **data augmentation** for better generalization.  
- Uses **Batch Normalization** for stability and faster convergence.  
- Supports **Dropout regularization** to prevent overfitting.  
- Trained on the **GTSRB dataset** (43 classes).  
- End-to-end notebook for easy reproducibility.

---

## 📘 Notebook

You can view or run the model training code in the Jupyter notebook provided:

📄 [`traffic_sign_classification.ipynb`](traffic_sign_classification.ipynb)

---

## ⚙️ Requirements

Install dependencies with:

```bash
pip install -r requirements.txt
```

---

## 🧾 Usage

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/yourusername/traffic-sign-cnn.git
cd traffic-sign-cnn
```

### 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 3️⃣ Run the Notebook

```bash
jupyter notebook traffic_sign_classification.ipynb
```

### 4️⃣ (Optional) Train or Evaluate

Adjust parameters and re-run training cells to fine-tune the model.

---

## 📊 Performance Metrics (example)

| Metric | Value |
|--------|--------|
| Training Accuracy | ~98% |
| Validation Accuracy | ~96% |
| Loss | 0.12 |

*(Actual results depend on dataset split and training epochs.)*

---

## 🧩 Possible Improvements

- Try deeper CNN or transfer learning with ResNet/VGG.  
- Apply learning rate schedulers or optimizers like AdamW.  
- Add early stopping and model checkpointing.  
- Experiment with grayscale vs RGB inputs.

---

## 📜 License

This project is open-source and available under the **MIT License**.

---

**Author:** Omar Ben Emad  
**Model:** Custom CNN  
**Framework:** TensorFlow / Keras  
**Dataset:** GTSRB (German Traffic Sign Recognition Benchmark)
