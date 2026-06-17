# Awesome-Latent-Diffusion-Models
## Latent Diffusion Models (LDMs): Types & Examples

**Latent Diffusion Models (LDMs)** are generative AI frameworks that perform the computationally heavy diffusion process inside a compressed "latent space" rather than raw pixel space. This vastly reduces computation requirements while maintaining high-fidelity generation.

---

## 🛠️ Categorized by Conditioning (Input Types)

LDMs adapt to user intent through several conditioning mechanisms that guide the generation process:

| Type | Description | Year | Paper Link |
| :--- | :--- | :--- | :--- |
| **Text-to-Image (T2I)** | Transforms a raw text prompt into a high-fidelity visual representation. | 2021 | [Rombach et al.](https://arxiv.org/abs/2112.10752) |
| **Class-Conditional** | Generates specific categories based on a label (e.g., conditioning on "Dog" or specific MNIST digits). | 2021 | [Rombach et al.](https://arxiv.org/abs/2112.10752) |
| **Image-to-Image (I2I)** | Modifies a source image using a text prompt while preserving core compositions. | 2021 | [Rombach et al.](https://arxiv.org/abs/2112.10752) |
| **Layout/Segmentation-to-Image** | Guides generation using geometric bounding boxes, layouts, or segmentation masks. | 2021 | [Rombach et al.](https://arxiv.org/abs/2112.10752) |
| **Spatial/Depth-to-Image** | Matches the physical geometry of an input using depth maps or edge maps. | 2021 | [Rombach et al.](https://arxiv.org/abs/2112.10752) |

---

## 🏗️ Popular Architecture Examples

| Model | Description | Year | Paper Link |
| :--- | :--- | :--- | :--- |
| **Stable Diffusion** | The most prominent open-source LDM. It uses a VAE to compress images and a frozen CLIP text encoder for conditioning. Variants include **SDXL** (high-res) and **SVD** (video). | 2021 | [Rombach et al.](https://arxiv.org/abs/2112.10752) |
| **LDM-VQ (Vector Quantized)** | Foundational implementations (like *LDM-VQ-4*) that utilize vector quantization in the autoencoder stage for categorical image synthesis. | 2021 | [Rombach et al.](https://arxiv.org/abs/2112.10752) |
| **LDM-KL (Kullback-Leibler)** | Models that utilize KL-regularization during the encoding phase to ensure a smooth, continuous latent distribution. | 2021 | [Rombach et al.](https://arxiv.org/abs/2112.10752) |

---

## 🚀 Specialized Task Examples

| Task | Description | Year | Paper Link |
| :--- | :--- | :--- | :--- |
| **Inpainting & Outpainting** | Masks out specific areas of an image to change elements, or extends the borders beyond the original canvas. | 2021 | [Rombach et al.](https://arxiv.org/abs/2112.10752) |
| **Super-Resolution / Denoising** | Takes low-resolution latent representations and decodes them into high-resolution outputs by predicting missing spatial details. | 2021 | [Rombach et al.](https://arxiv.org/abs/2112.10752) |

---

## 🧬 Recent Advancements 

| Advancement | Description | Year | Paper Link |
| :--- | :--- | :--- | :--- |
| **Latent Causal Diffusion Models (LacaDM)** | Advanced frameworks that integrate structural causal models to allow for precise causal interventions and counterfactual reasoning. | 2025 | [Zhang et al.](https://arxiv.org/abs/2512.19516) |
| **Fast Decoders (e.g., PiD)** | New paradigms replacing traditional autoencoder decoders with conditional pixel-space diffusion modules (Pixel Diffusion Decoder). | 2026 | [NVIDIA (PiD)](https://arxiv.org/abs/2605.23902) |
