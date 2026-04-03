# Indoor-Scene-Image-Generation-using-DCGAN

🌆 Project 6: Indoor Scene Image Generation using DCGAN

A complete end-to-end system that uses Deep Convolutional GANs (DCGANs) to generate realistic indoor scene images from the MIT Indoor Dataset.

This project demonstrates how GANs can learn complex indoor environments such as malls, offices, meeting rooms, and more, and generate synthetic images for research and data augmentation purposes.

📌 Why this project?

Indoor scene classification datasets often face:

Limited labeled data for certain categories
Class imbalance (some scenes underrepresented)
High cost of collecting and labeling real images

Traditional augmentation techniques (flip, rotate) are limited and cannot generate new realistic environments.

👉 This project solves:
How can GANs generate realistic indoor scene images to improve dataset diversity?

🧭 What does this project do?
Trains a DCGAN model on MIT Indoor Dataset
Learns complex indoor scene structures
Generates realistic synthetic indoor images
Preprocesses images using TensorFlow pipeline
Produces generated samples during training
Saves outputs for visualization and evaluation

🧠 System Overview
MIT Indoor Dataset
        ↓
Data Preprocessing
        ↓
DCGAN Training
        ↓
Synthetic Indoor Images
        ↓
Visualization & Evaluation

📁 Project Structure
Project6/
├── data/
│   └── Images/                  # Indoor dataset images
├── checkpoints/                # Saved model weights
├── logs/                       # Training logs
├── samples/                    # Generated images
├── notebooks/
│   └── GANI_Project6.ipynb     # Main notebook
├── README.md

📦 Dataset
Dataset Used: MIT Indoor Scene Dataset
Contains multiple categories such as:
mall
office
meeting_room
movietheater
kitchen
bedroom

🧩 Model Architecture
🔹 Generator
Input: Random noise vector (z)
Uses:
ConvTranspose2D
Batch Normalization
ReLU activation
Output: 128×128 RGB image
🔹 Discriminator
Input: Image (real or fake)
Uses:
Conv2D layers
LeakyReLU
Batch Normalization
Output: Real/Fake probability

🔁 Training Process

Each training step:
Load real images
Generate fake images from noise
Train discriminator on real + fake
Train generator to fool discriminator

⚙️ Preprocessing
Resize images to fixed size (128×128)
Normalize pixel values to [-1, 1]
Apply random horizontal flipping

▶️ How to Run
1. Mount Google Drive
from google.colab import drive
drive.mount('/content/drive')
2. Load Dataset
with open(TRAIN_SPLIT_FILE, 'r') as f:
    lines = f.read().splitlines()
3. Train Model

📊 Outputs
Generated indoor scene images
Training loss graphs
Batch-wise image samples

🖼️ Sample Outputs
Synthetic malls
Office environments
Meeting rooms
Theaters

⚠️ Limitations
No class conditioning (cannot control scene type)
Image resolution limited
GAN instability possible during training

🔮 Future Improvements
Conditional GAN (cGAN)
Higher resolution (256×256)
StyleGAN for better realism
Class-specific generation

🎯 Final Result
✔ Same professional format as your faculty example
✔ Customized for your Project 6
✔ Ready to submit
