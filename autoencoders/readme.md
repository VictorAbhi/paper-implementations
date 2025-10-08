**Paper 1 Classic Autoencoder**
Reducing the Dimensionality of Data with Neural Networks (Hinton & Salakhutdinov, Science 2006)

**Idea**: Train a neural net to compress and reconstruct data.
**Learning**: Basic encoder–decoder structure, latent representation, reconstruction loss (MSE).
**Implementation**: Train on MNIST
<hr>

**Paper 2 Denoising Autoencoder**

Extracting and Composing Robust Features with Denoising Autoencoders (Vincent et al., ICML 2008)

**Idea**: Corrupt input (e.g., add Gaussian noise) and train autoencoder to recover clean input.
**Learning**: Robust feature learning, noise tolerance.
**Implementation**: Add random noise to MNIST digits and reconstruct the original.

Regular Autoencoder: minimize ||x - decoder(encoder(x))||²

Denoising Autoencoder: minimize ||x - decoder(encoder(C(x)))||²
                    where C(x) is the corrupted version of x

**Paper 3 Sparse Autoencoder**
Sparse Autoencoder for Feature Learning (Ng, 2011 tutorial)

**Idea**: Encourage sparsity in hidden activations (via KL divergence or L1 regularization).

**Learning**: How sparsity encourages useful features, prevents trivial identity mapping.

**Implementation**: Add sparsity penalty to autoencoder trained on MNIST.

***Paper 4 Variational Autoencoder**
Auto-Encoding Variational Bayes (Kingma & Welling, ICLR 2014)

**Idea**: Probabilistic autoencoder → learns a distribution of latent variables.

**Learning**: Latent variable models, reparameterization trick, KL divergence.

**Implementation**: Train a VAE on MNIST, sample new digits from the latent space.

***Paper 5 Beta Variational Autoencoder**
β-VAE: Learning Basic Visual Concepts with a Constrained Variational Framework (Higgins et al., ICLR 2017)

**Idea**: Add a hyperparameter β to control trade-off between reconstruction and disentanglement.

**Learning**: How to discover disentangled representations.

**Implementation**: Train on dSprites or CelebA, visualize latent traversal (changing one latent at a time).