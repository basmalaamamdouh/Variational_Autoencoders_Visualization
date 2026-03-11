β-VAE Face Explorer
<img width="1909" height="846" alt="image" src="https://github.com/user-attachments/assets/47ad67a6-84b8-417a-8406-c8d026fc41cc" />

An interactive web app for exploring the latent space of a β-Variational Autoencoder trained on CelebA faces.

The model compresses faces into a 16-dimensional latent vector.
By changing those values, you can see how different attributes affect the generated face.

Live Demo:
https://basmalaamamdouh.github.io/Variational_Autoencoders_Visualization/

Features

Control facial attributes using semantic sliders

Random face generation

Interpolation between faces

Visualize the 16-dimensional latent vector

Export generated faces as PNG

Runs fully in the browser using ONNX Runtime (no backend)

Model
Parameter	Value
Model	β-Variational Autoencoder
Dataset	CelebA
Latent Dimensions	16
β	4
Image Size	64×64
Framework	PyTorch → ONNX

Attributes explored include:

Smiling • Young • Male • Eyeglasses • Bald • Blond Hair • Pale Skin • Heavy Makeup • Wearing Hat • Wavy Hair

Model Weights

The ONNX model is larger than GitHub’s file size limit.

Download it here:
ONNX Model

Load the file in the Load Files tab of the app.

Run Locally

Clone the repo:

git clone https://github.com/yourusername/vae-face-explorer

Open:

index.html

in Chrome or Edge and load:

vae_decoder.onnx

attr_vectors.json

Tech Stack

PyTorch (training)

ONNX Runtime Web (inference)

HTML / CSS / JavaScript (frontend)

Kaggle GPU (training)

Files
index.html
attr_vectors.json
notebook.ipynb
README.md

vae_decoder.onnx is hosted externally due to GitHub size limits.

License

MIT
