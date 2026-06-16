# Awesome-Latent-Diffusion-Models
## Latent Diffusion Models (LDMs): Types & Examples

**Latent Diffusion Models (LDMs)** are generative AI frameworks that perform the computationally heavy diffusion process inside a compressed "latent space" rather than raw pixel space. This vastly reduces computation requirements while maintaining high-fidelity generation.

---

## 🛠️ Categorized by Conditioning (Input Types)

LDMs adapt to user intent through several conditioning mechanisms that guide the generation process:

* **Text-to-Image (T2I):** Transforms a raw text prompt into a high-fidelity visual representation. 
* **Class-Conditional:** Generates specific categories based on a label (e.g., conditioning on "Dog" or specific MNIST digits).
* **Image-to-Image (I2I):** Modifies a source image using a text prompt while preserving core compositions.
* **Layout/Segmentation-to-Image:** Guides generation using geometric bounding boxes, layouts, or segmentation masks.
* **Spatial/Depth-to-Image:** Matches the physical geometry of an input using depth maps or edge maps.

---

## 🏗️ Popular Architecture Examples

* **Stable Diffusion:** The most prominent open-source LDM. It uses a Variational Autoencoder (VAE) to compress images and a frozen CLIP text encoder for text-based conditioning. Variations include:
  * **Stable Diffusion XL (SDXL):** Optimized for higher resolution and photorealism.
  * **Stable Video Diffusion (SVD):** Adapted for generating moving content and short video clips.
* **LDM-VQ (Vector Quantized):** Foundational implementations (like *LDM-VQ-4*) that utilize vector quantization in the autoencoder stage for categorical image synthesis.
* **LDM-KL (Kullback-Leibler):** Models that utilize KL-regularization during the encoding phase to ensure a smooth, continuous latent distribution (commonly used in scene generation tasks like churches or bedrooms).

---

## 🚀 Specialized Task Examples

* **Inpainting & Outpainting:** Masks out specific areas of an image to change elements, or extends the borders beyond the original canvas by intelligently guessing missing spaces.
* **Super-Resolution / Denoising:** Takes low-resolution latent representations and decodes them into high-resolution outputs by predicting missing spatial details.

---

## 🧬 Recent Advancements 

* **Latent Causal Diffusion Models (LacaDM):** Advanced frameworks that integrate structural causal models to allow for precise causal interventions and counterfactual reasoning rather than purely aesthetic generation. 
* **Fast Decoders (e.g., PiD):** New paradigms replacing traditional autoencoder decoders with conditional pixel-space diffusion modules, allowing latent representations to be processed into high-resolution images in a single pass.
