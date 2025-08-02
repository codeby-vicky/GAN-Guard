# 🚨 GAN-Guard: Proactive Anomaly Detection in Surveillance using GANs

## 🧠 Project Overview

**GAN-Guard** is a *proactive anomaly detection system* designed for real-time surveillance using **Generative Adversarial Networks (GANs)**. It learns typical visual patterns from normal surveillance footage and identifies deviations (anomalies) in live video streams. On detecting an anomaly, **YOLO (You Only Look Once)** is triggered to detect and label objects in the scene for enhanced situational awareness.

## ✅ Key Features

- Trained on 40 normal surveillance images using GAN to model typical behavior.
- Real-time video input processing via **OpenCV** (webcam or CCTV feed).
- Detects anomalies by comparing current frames against learned norms.
- Integrates **YOLO** for object detection when anomalies occur.
- Fast, lightweight, and suitable for edge deployment.

## 🧰 Technologies Used

- **Python**
- **OpenCV** – for video capture and manipulation
- **TensorFlow / PyTorch** – for implementing GAN
- **YOLO (v3/v4/v5)** – for object detection on flagged frames
- **NumPy, Matplotlib** – for processing and visualization

## 🔍 How It Works

### 1. Training Phase

- GAN is trained with 40 "normal" surveillance images.
- The generator learns to replicate standard surveillance scenarios.
- The discriminator differentiates between real and generated images, improving accuracy.

### 2. Detection Phase

- Live frames are captured using OpenCV.
- Each frame is evaluated against the learned GAN model.
- Frames with significant deviation (anomalies) are flagged.
- YOLO is executed on the flagged frame to identify and label objects for further review.

## ⚙️ Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone https://github.com/vignesh33-ui/GAN-Guard.git
   cd GAN-Guard
````

2. **Install Dependencies**

   ```bash
   pip install -r requirements.txt
   ```

3. **Add Training Data**
   Place your normal surveillance images into the `training_data/` folder.

4. **Train the GAN**

   ```bash
   python train_gan.py
   ```

5. **Run Live Anomaly Detection**

   ```bash
   python detectano.py
   ```

## 📁 Folder Structure

```
GAN-Guard/
│
├── training_data/         # Folder containing normal images
├── gan_model/             # Trained GAN model weights
├── yolo/                  # YOLO configuration and weights
├── traingan.py            # GAN training script
├── detectano.py           # Real-time anomaly detection script
├── rename.py              # Utility script
└── README.md              # Project documentation
```

## 📸 Demo 

![screenshots](screenshots\Picture1.jpg)

## 👨‍💻 Author

**Vignesh M N**
[LinkedIn](https://www.linkedin.com/in/vignesh-m-n-3b5282270) | [GitHub](https://github.com/codeby-vicky)

```


