# Awesome-Latent-Diffusion-Models
## Latent Diffusion Models (LDMs): Types & Examples

**Latent Diffusion Models (LDMs)** are generative AI frameworks that perform the computationally heavy diffusion process inside a compressed "latent space" rather than raw pixel space. This vastly reduces computation requirements while maintaining high-fidelity generation.

---

## 🛠️ Categorized by Conditioning (Input Types)

LDMs adapt to user intent through several conditioning mechanisms that guide the generation process:

| Type | Description | Year | Paper Link | Details |
| :--- | :--- | :--- | :--- | :--- |
| **[Text-to-Image (T2I)](docs/t2i.md)** | Transforms a raw text prompt into a high-fidelity visual representation using cross-attention. | 2021 | [Rombach et al.](https://arxiv.org/abs/2112.10752) | [View Doc](docs/t2i.md) |
| **[Class-Conditional](docs/class-conditional.md)** | Generates specific categories based on a label (e.g., conditioning on "Dog" or specific MNIST digits). | 2021 | [Rombach et al.](https://arxiv.org/abs/2112.10752) | [View Doc](docs/class-conditional.md) |
| **[Image-to-Image (I2I)](docs/i2i.md)** | Modifies a source image using a text prompt while preserving core compositions and structure. | 2021 | [Rombach et al.](https://arxiv.org/abs/2112.10752) | [View Doc](docs/i2i.md) |
| **[Layout/Segmentation-to-Image](docs/layout-to-image.md)** | Guides generation using geometric bounding boxes, layouts, or semantic segmentation masks. | 2021 | [Rombach et al.](https://arxiv.org/abs/2112.10752) | [View Doc](docs/layout-to-image.md) |
| **[Spatial/Depth-to-Image](docs/spatial-to-image.md)** | Matches the physical geometry of an input using depth maps, edge maps (Canny), or normal maps. | 2021 | [Rombach et al.](https://arxiv.org/abs/2112.10752) | [View Doc](docs/spatial-to-image.md) |

---

## 🏗️ Popular Architecture Examples

| Model | Description | Year | Paper Link | Details |
| :--- | :--- | :--- | :--- | :--- |
| **[Stable Diffusion](docs/stable-diffusion.md)** | The most prominent open-source LDM. It uses a VAE to compress images and a frozen CLIP text encoder for conditioning. | 2021 | [Rombach et al.](https://arxiv.org/abs/2112.10752) | [View Doc](docs/stable-diffusion.md) |
| **[LDM-VQ (Vector Quantized)](docs/ldm-vq.md)** | Foundational implementations (like *LDM-VQ-4*) that utilize vector quantization in the autoencoder stage. | 2021 | [Rombach et al.](https://arxiv.org/abs/2112.10752) | [View Doc](docs/ldm-vq.md) |
| **[LDM-KL (Kullback-Leibler)](docs/ldm-kl.md)** | Models that utilize KL-regularization during the encoding phase to ensure a smooth, continuous latent distribution. | 2021 | [Rombach et al.](https://arxiv.org/abs/2112.10752) | [View Doc](docs/ldm-kl.md) |

---

## 🚀 Specialized Task Examples

| Task | Description | Year | Paper Link | Details |
| :--- | :--- | :--- | :--- | :--- |
| **[Inpainting & Outpainting](docs/inpainting-outpainting.md)** | Masks out specific areas of an image to change elements, or extends the borders beyond the original canvas. | 2021 | [Rombach et al.](https://arxiv.org/abs/2112.10752) | [View Doc](docs/inpainting-outpainting.md) |
| **[Super-Resolution / Denoising](docs/super-res.md)** | Takes low-resolution latent representations and decodes them into high-resolution outputs with fine details. | 2021 | [Rombach et al.](https://arxiv.org/abs/2112.10752) | [View Doc](docs/super-res.md) |

---

## 🧬 Recent Advancements 

| Advancement | Description | Year | Paper Link | Details |
| :--- | :--- | :--- | :--- | :--- |
| **[Latent Causal Diffusion Models (LacaDM)](docs/lacadm.md)** | Advanced frameworks that integrate structural causal models to allow for precise causal interventions. | 2025 | [Zhang et al.](https://arxiv.org/abs/2512.19516) | [View Doc](docs/lacadm.md) |
| **[Fast Decoders (e.g., PiD)](docs/pid.md)** | New paradigms replacing traditional VAE decoders with conditional pixel-space diffusion modules (Pixel Diffusion Decoder). | 2026 | [NVIDIA (PiD)](https://arxiv.org/abs/2605.23902) | [View Doc](docs/pid.md) |
