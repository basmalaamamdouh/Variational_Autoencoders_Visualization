# Virtual-AutoEncoders-Visualization
#  β-VAE Face Explorer

An interactive browser app for exploring a **16-dimensional disentangled latent space** 
trained on CelebA faces using a β-Variational Autoencoder (β=4).

**Live demo → [Try it here]("https://sweet-sharing-hub.lovable.app"))**

---

## What is this?

A β-VAE is a type of generative model that learns to compress images into a small 
latent vector where each dimension captures an independent factor of variation 
(smile, age, gender, hair color, etc.). This app lets you explore that latent space 
interactively in the browser — no server, no GPU needed.

---

## Features

-  **Semantic sliders** — edit Smiling, Age, Gender, Eyeglasses, Hair and more
-  **Random generation** — sample new faces from the latent space
-  **Interpolation** — morph smoothly between two faces
-  **Latent visualizer** — see all 16 dimensions update in real time
-  **Save** — export faces as 512×512 PNG
-  **100% in-browser** — powered by ONNX Runtime Web, no backend needed

---

## Download Model Weights

The ONNX model is too large for GitHub (>25MB). Download it from Google Drive:

👉 **[Download vae_decoder.onnx](https://drive.google.com/file/d/1SEoKEIkrHNMYSYc1BM14rJgs0m_P0HWH/view?usp=sharing)**

After downloading, load it in the app via the **Load Files** tab.

---

## How to use

### Option A — Live Demo (recommended)
1. Open the [live demo](https://sweet-sharing-hub.lovable.app)
2. Go to **Load Files** tab
3. Click Browse next to `vae_decoder.onnx` → select the file downloaded from Google Drive above
4. Click Browse next to `attr_vectors.json` → select it from the repo
5. App switches to **Semantic** tab and generates a face automatically

### Option B — Run locally
1. Clone this repo
2. Download `vae_decoder.onnx` from the Google Drive link above
3. Place it in the same folder as `index.html`
4. Open `index.html` in Chrome or Edge
5. Load both files via the **Load Files** tab

---

## Model Details

| Parameter | Value |
|-----------|-------|
| Architecture | β-VAE with ResBlocks |
| Dataset | CelebA (200k images) |
| Latent dimensions | 16 |
| β (disentanglement) | 4 |
| Image size | 64×64 |
| Training epochs | 35 |
| Best val loss | 711.08 |
| Framework | PyTorch → ONNX |

### Tracked Attributes
Smiling · Young · Male · Eyeglasses · Bald · Blond Hair · Pale Skin · Heavy Makeup · Wearing Hat · Wavy Hair

---

## Run training yourself

The full training notebook is included: `notebook.ipynb`

Designed for **Kaggle T4 GPU** (~2.5 hours):

1. Upload to Kaggle
2. Add the [CelebA dataset](https://www.kaggle.com/datasets/jessicali9530/celeba-dataset)
3. Run all cells in order
4. Download `vae_decoder.onnx` and `attr_vectors.json` from the Output tab

---

## Tech Stack

- **Training** — PyTorch, CelebA dataset, Kaggle T4 GPU
- **Export** — ONNX (opset 17)
- **Frontend** — Vanilla HTML/CSS/JS
- **Inference** — [ONNX Runtime Web](https://onnxruntime.ai/)
- **Attribute discovery** — PCA + Logistic Regression on latent means

---

## Project Structure
```
├── index.html          # Web app (self-contained)
├── attr_vectors.json   # Semantic directions in latent space
├── notebook.ipynb      # Full training code
└── README.md           # This file
```

> `vae_decoder.onnx` is hosted on Google Drive due to GitHub's 25MB file limit.

---

## License
MIT
