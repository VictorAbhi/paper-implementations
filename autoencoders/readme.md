#  Autoencoder Paper Implementations

This repository contains implementations of fundamental **Autoencoder architectures** from classic to modern variants, focusing on understanding their core ideas, mathematical foundations, and experimental behavior.

---

## **Paper 1 — Classic Autoencoder**
📄 *Reducing the Dimensionality of Data with Neural Networks*  
**Authors:** Hinton & Salakhutdinov, *Science, 2006*  

**Idea:**  
Train a neural network to compress and reconstruct data through a bottleneck layer.

**Learning Outcomes:**  
- Understand encoder–decoder architecture  
- Learn latent representation and reconstruction loss (MSE)  

**Implementation:**  
Train an Autoencoder on MNIST dataset to reduce dimensionality.

---

## **Paper 2 — Denoising Autoencoder**
📄 *Extracting and Composing Robust Features with Denoising Autoencoders*  
**Authors:** Vincent et al., *ICML, 2008*  

**Idea:**  
Corrupt input data (e.g., add Gaussian noise) and train the network to recover the clean input.

**Learning Outcomes:**  
- Learn robust feature extraction  
- Build noise-tolerant representations  

**Objective Functions:**
Regular AE: minimize ||x - decoder(encoder(x))||²
Denoising AE: minimize ||x - decoder(encoder(C(x)))||²
where C(x) is the corrupted version of x

**Implementation:**  
Add random noise to MNIST digits and reconstruct the clean originals.

---

## **Paper 3 — Sparse Autoencoder**
📄 *Sparse Autoencoder for Feature Learning*  
**Author:** Andrew Ng, *Tutorial, 2011*  

**Idea:**  
Encourage sparsity in hidden activations using a penalty term (L1 regularization or KL divergence).

**Learning Outcomes:**  
- Understand how sparsity improves feature learning  
- Avoid trivial identity mapping  

**Implementation:**  
Train an Autoencoder on MNIST with a sparsity penalty in the loss function.

---

## **Paper 4 — Variational Autoencoder (VAE)**
📄 *Auto-Encoding Variational Bayes*  
**Authors:** Kingma & Welling, *ICLR, 2014*  

**Idea:**  
Model the latent space as a probability distribution — enabling sampling and generation.

**Learning Outcomes:**  
- Latent variable models  
- Reparameterization trick  
- KL divergence regularization  

**Implementation:**  
Train a VAE on MNIST and sample new digits from the learned latent space.

---

## **Paper 5 — β-VAE (Beta Variational Autoencoder)**
📄 *β-VAE: Learning Basic Visual Concepts with a Constrained Variational Framework*  
**Authors:** Higgins et al., *ICLR, 2017*  

**Idea:**  
Introduce a hyperparameter **β** to balance reconstruction accuracy and latent disentanglement.

**Learning Outcomes:**  
- Understand disentangled representation learning  
- Explore reconstruction vs. compression trade-off  

**Implementation:**  
Train on **dSprites** or **CelebA**, and visualize latent traversal by varying one latent variable at a time.

---

## **Paper 6 — Adversarial Autoencoder (AAE)**
📄 *Adversarial Autoencoders*  
**Authors:** Makhzani et al., *ICLR, 2016*  

**Idea:**  
Combine Autoencoders with adversarial (GAN-style) training to match the latent space to a prior distribution.

**Learning Outcomes:**  
- Adversarial regularization of latent space  
- Relationship between GANs and Autoencoders  

**Implementation:**  
Train an AAE on MNIST to enforce the latent space ≈ Normal(0, 1), and sample new digits.

---

## **Paper 7 — Seq2Seq Autoencoder (for NLP)**
📄 *Sequence to Sequence Learning with Neural Networks*  
**Authors:** Sutskever et al., *NIPS, 2014*  

**Idea:**  
An Encoder RNN compresses input sequences into a context vector; a Decoder RNN reconstructs or predicts the output sequence.

**Learning Outcomes:**  
- Sequence compression and reconstruction  
- Foundation for translation and conversational models  

**Implementation:**  
Train an RNN-based Seq2Seq Autoencoder on short text sequences (toy dataset).

---

## Summary of Concepts
| Paper | Core Idea | Key Concept | Dataset |
|--------|------------|--------------|----------|
| 1 | Classic Autoencoder | Dimensionality reduction | MNIST |
| 2 | Denoising AE | Robust feature learning | MNIST |
| 3 | Sparse AE | Sparse hidden activations | MNIST |
| 4 | Variational AE | Probabilistic latent modeling | MNIST |
| 5 | β-VAE | Disentanglement control | dSprites / CelebA |
| 6 | Adversarial AE | GAN-style latent regularization | MNIST |
| 7 | Seq2Seq AE | Sequence encoding & decoding | Text (IMDb/Toy) |

---

💡 *Goal:* To build an intuitive and practical understanding of Autoencoders — from basic compression to probabilistic, adversarial, and sequence-based models — forming a foundation for modern generative and representation learning research.
