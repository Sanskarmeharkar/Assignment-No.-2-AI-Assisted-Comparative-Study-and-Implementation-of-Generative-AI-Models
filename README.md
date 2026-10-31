# Assignment-No.-2-AI-Assisted-Comparative-Study-and-Implementation-of-Generative-AI-Models
# Comparative Study of Generative AI Models (AE, VAE, DCGAN, Diffusion)

Internal Assignment 02, MIT Academy of Engineering.

**Group:**
- Sanskar Ramesh Meharkar (202401110029)
- Meghana Shirish Innani (202401110009)
- Dewesh Barapatre (202401110053)

## About
This project compares four generative models on face images from the
**LFW (Labeled Faces in the Wild)** dataset (4,000 images, 64×64 RGB):

- Autoencoder (AE): trained from scratch
- Variational Autoencoder (VAE): trained from scratch
- DCGAN: trained from scratch
- Pretrained diffusion model (`segmind/tiny-sd`): inference only

## Results

| Model | Time | MSE | PSNR (dB) | SSIM |
|---|---|---|---|---|
| AE | 37.3 s | 0.01030 | 20.24 | 0.5988 |
| VAE | 34.9 s | 0.02337 | 16.60 | 0.4194 |
| DCGAN | 138.8 s | – | – | – |
| Diffusion | 2.03 s per image | – | – | – |

- The AE reconstructs faces more faithfully than the VAE, which gives smoother, blurrier faces.
- The DCGAN produces blurry, face-like 64×64 images.
- The diffusion model produces the most realistic 512×512 portraits, but it is pretrained, so the comparison is not like-for-like.

## Run it
1. Open the notebook in Google Colab: [Open in Colab](https://colab.research.google.com/drive/1fm5EdQ33McorXnu9g1bgzVHw_6xQ9uq4?usp=sharing)
2. Set the runtime to GPU (Runtime > Change runtime type > T4 GPU).
3. Choose Runtime > Run all (about 10–20 minutes).

## Files
- `GenAI_Assignment02_LFW_Notebook.ipynb`: code and outputs
- `GenAI_Assignment02_Report.pdf`: full report

## Tools
Python, TensorFlow/Keras, PyTorch, Hugging Face Diffusers, Google Colab.
AI assistance: Claude (used for explanations, debugging and report writing).
