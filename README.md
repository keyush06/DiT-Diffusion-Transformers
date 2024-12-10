# DiT-Diffusion-Transformers
Implementation of transformers as a backbone feature extractor

#### This repository contains the implementation of PatchVAE, enhanced by incorporating diffusion models to improve the realism and quality of generated images. This project explores the intersection of Variational Autoencoders (VAE) and Diffusion Models, highlighting how diffusion can address the limitations of VAEs and produce more realistic and visually pleasing outputs.

**PatchVAE**
PatchVAE is a variant of the Variational Autoencoder that introduces a patch-based approach to image synthesis. Instead of processing the entire image as a single unit, PatchVAE divides the image into smaller, non-overlapping patches and applies VAE operations on these patches. This approach aims to capture fine-grained, localized features that are often missed by traditional VAEs.

While PatchVAE improves the ability to learn local features, the synthesized images often lack global coherence and realism. This is where Diffusion Models come into play.

**Diffusion Models**
Diffusion models are generative models that progressively transform simple distributions (e.g., Gaussian noise) into complex data distributions (e.g., images). They achieve this through a series of denoising steps that reconstruct images from noise.

_In this project, we use diffusion models to refine the outputs of PatchVAE. By combining the strengths of PatchVAE's localized feature learning with the global coherence brought by diffusion models, we achieve superior results._

### **How Diffusion Improves PatchVAE**
**Addressing Global Coherence:** PatchVAE's patch-based approach can result in disjointed or inconsistent global features. Diffusion models smooth these inconsistencies, ensuring that the synthesized images are globally coherent while maintaining the high-quality local details.

**Enhancing Realism:** Diffusion models generate images through a step-by-step process that allows for realistic reconstruction. This iterative refinement eliminates artifacts and improves the overall quality of the images.

**Improved Diversity:** By combining the latent features from PatchVAE with diffusion's ability to explore a wide range of data distributions, the model produces more diverse and representative samples.
