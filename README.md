# Image Generation | Summer of Science 2026

This repository contains the study notes, implementations, and experimental results from the first four weeks of the Image Generation project under Summer of Science 2026. The project focuses on deep learning foundations, generative models, and practical implementations of GAN-based image generation techniques using PyTorch.

## Progress Summary (Week 4)

### Completed
- Deep Learning Foundations
- CNN Basics and PyTorch
- GAN Theory
- Vanilla GAN Implementation (MNIST)
- DCGAN Implementation (CIFAR-10)
- CycleGAN Literature Review

### Upcoming
- CycleGAN Implementation
- StyleGAN and StyleGAN2
- Diffusion Models (DDPM)
- Comparative Evaluation of Generative Models

---

## Repository Structure

```text
├── GAN.ipynb
├── DCGAN.ipynb
├── outputs/
│   ├── vanilla_generated.png
│   ├── vanilla_loss.png
│   ├── dcgan_generated.png
│   └── dcgan_loss.png
└── README.md
```

## Week 1 — Deep Learning Foundations

### Topics Covered

- Neural networks, backpropagation, and gradient descent
- Activation functions: ReLU, Leaky ReLU, Sigmoid, and Tanh
- Convolutional Neural Networks (CNNs)
- Convolution operations, strided convolutions, and transposed convolutions
- Batch Normalization
- Image representation as tensors
- PyTorch fundamentals
- Google Colab GPU workflows

---

## Week 2 — GAN Theory

### Topics Covered

- Introduction to generative modelling
- Generator and Discriminator architecture
- Adversarial training
- Latent space representations
- GAN objective function
- Non-saturating generator loss
- Jensen-Shannon divergence intuition

### Training Instability Issues

- Mode collapse
- Vanishing gradients
- Discriminator dominance

---

## Week 3 — Implementation

### Vanilla GAN on MNIST

#### Architecture

- Generator: Fully connected network with LeakyReLU and Tanh output
- Discriminator: Fully connected network with LeakyReLU, Dropout, and Sigmoid output

#### Training Setup

- Dataset: MNIST
- Loss Function: BCE
- Optimizer: Adam
- Learning Rate: 0.0002
- Batch Size: 128

#### Observations

- Generated images gradually resembled handwritten digits
- Early outputs were noisy and blurry
- Training instability was observed when the discriminator became significantly stronger than the generator

### DCGAN on CIFAR-10

#### Key Architectural Features

- Strided convolutions in the discriminator
- Transposed convolutions in the generator
- Batch Normalization
- ReLU activations in the generator
- LeakyReLU activations in the discriminator

#### Training Setup

- Dataset: CIFAR-10
- Optimizer: Adam
- Learning Rate: 0.0002
- Batch Size: 128

#### Observations

- Generated images showed improved spatial structure compared to Vanilla GAN
- Color distributions became more coherent during training
- Convolutional architectures produced noticeably better outputs than fully connected networks

---

## Week 4 — CycleGAN Theory

### Topics Covered

- Unpaired image translation
- Domain adaptation
- Cycle consistency loss
- Style transfer concepts
- Generator–Discriminator architecture in CycleGAN

### Applications Studied

- Horse ↔ Zebra
- Summer ↔ Winter
- Day ↔ Night
- Photo ↔ Monet-style translation

---

## Key Learnings

- Understanding adversarial learning is crucial for image generation
- Generator–Discriminator balance strongly affects training behaviour
- Convolutional architectures significantly improve image quality
- Batch Normalization helps stabilize GAN training
- Image-to-image translation extends generative modelling beyond image synthesis

---

## Future Work

### Week 5

- Implementation and experimentation with CycleGAN
- Study of StyleGAN and StyleGAN2 architectures
- Understanding adaptive instance normalization (AdaIN) and latent disentanglement

### Week 6

- StyleGAN experimentation
- Latent space exploration and interpolation
- Generated image quality analysis

### Week 7

- Introduction to Diffusion Models (DDPM)
- Understanding forward and reverse diffusion processes
- Noise scheduling and denoising-based generation

### Week 8

- Comparative evaluation of GANs, StyleGANs, and Diffusion Models
- Analysis of training stability, computational requirements, and output quality
- Final project refinement

---

## References

1. Goodfellow et al. (2014) — Generative Adversarial Networks
2. Radford et al. (2015) — Deep Convolutional GANs (DCGAN)
3. Zhu et al. (2017) — CycleGAN
4. Andrew Ng — Deep Learning Specialization
5. PyTorch Documentation
6. PyTorch DCGAN Tutorial
