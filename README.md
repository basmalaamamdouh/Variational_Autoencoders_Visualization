β-VAE Face Explorer
<img width="1909" height="846" alt="β-VAE Face Explorer Screenshot" src="https://github.com/user-attachments/assets/47ad67a6-84b8-417a-8406-c8d026fc41cc" />

Explore the hidden features of human faces with AI.
This project is an interactive web app that lets you play with the latent space of a β-Variational Autoencoder (β-VAE) trained on thousands of CelebA faces.

The β-VAE compresses each face into a 16-dimensional vector, where each number represents a meaningful facial attribute. By adjusting these values, you can change expressions, hairstyles, age, and more, and see the face transform in real-time.

Try it live: https://basmalaamamdouh.github.io/Variational_Autoencoders_Visualization/

- Key Features

Interactive Sliders: Control facial attributes like smiling, age, hair color, and accessories.

Random Face Generation: Instantly create new faces from the learned latent space.

Face Interpolation: Smoothly transition between two faces to explore variations.

Latent Space Visualization: See the 16-dimensional vector behind each face.

Export Faces: Save generated faces as PNG images.

Fully Browser-Based: No backend required, powered by ONNX Runtime Web.

🔬 How It Works

Training:
The β-VAE is trained on the CelebA dataset to encode faces into a compact latent space.

Latent Space:
Each face is represented as a 16-dimensional vector. Changing a value changes a specific attribute in the face (like smiling or age).

Decoding:
The latent vector is fed into a decoder (ONNX model) to generate the face image in real-time.

Explorable Attributes: Smiling • Young • Male • Eyeglasses • Bald • Blond Hair • Pale Skin • Heavy Makeup • Wearing Hat • Wavy Hair

⚙️ Tech Stack

PyTorch: Model training

ONNX Runtime Web: Real-time inference in the browser

HTML / CSS / JavaScript: Frontend

Kaggle GPU: Model training environment

- Model Weights

The model file is too large for GitHub, so download it here:
Download β-VAE ONNX Model

Load it in the app’s Load Files tab to start exploring.

- Run Locally

Clone the repo:

git clone https://github.com/yourusername/vae-face-explorer

Open index.html in your browser.

Load the following files:

vae_decoder.onnx

attr_vectors.json

- Project Files
index.html
attr_vectors.json
notebook.ipynb
README.md
- Why This Project?

This project demonstrates the power of disentangled latent spaces in generative models. It’s a hands-on way to understand how AI can encode complex features into simple numbers, allowing interactive manipulation of human faces — something that’s at the heart of research in computer vision and creative AI applications.
___
 License

MIT
