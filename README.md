<div align="center">
  <img src="assets/banner.svg" alt="Awesome Latent Diffusion Models Banner" width="800" />
  
  <p align="center">
    <a href="https://github.com/ishandutta2007/Awesome-Latent-Diffusion-Models/stargazers"><img src="https://img.shields.io/github/stars/ishandutta2007/Awesome-Latent-Diffusion-Models?style=for-the-badge&color=yellow" alt="stars" /></a>
    <a href="https://github.com/ishandutta2007/Awesome-Latent-Diffusion-Models/network/members"><img src="https://img.shields.io/github/forks/ishandutta2007/Awesome-Latent-Diffusion-Models?style=for-the-badge&color=blue" alt="forks" /></a>
    <a href="https://github.com/ishandutta2007/Awesome-Latent-Diffusion-Models/issues"><img src="https://img.shields.io/github/issues/ishandutta2007/Awesome-Latent-Diffusion-Models?style=for-the-badge&color=red" alt="issues" /></a>
    <a href="https://github.com/ishandutta2007/Awesome-Latent-Diffusion-Models/pulls"><img src="https://img.shields.io/github/issues-pr/ishandutta2007/Awesome-Latent-Diffusion-Models?style=for-the-badge&color=green" alt="pull requests" /></a>
    <a href="https://github.com/ishandutta2007/Awesome-Latent-Diffusion-Models/blob/main/LICENSE"><img src="https://img.shields.io/github/license/ishandutta2007/Awesome-Latent-Diffusion-Models?style=for-the-badge" alt="license" /></a>
    <a href="https://github.com/ishandutta2007"><img alt="GitHub followers" src="https://img.shields.io/github/followers/ishandutta2007?label=Follow&style=for-the-badge" /></a>
  </p>

  <h3>🌟 A Curated List of Latent Diffusion Model (LDM) Architectures, Techniques, and Applications</h3>
</div>

<!-- SEO Tags -->
<!-- Keywords: Latent Diffusion Models, Stable Diffusion, LDM, Generative AI, Text-to-Image, AI Research, Computer Vision, Diffusion Models, LacaDM, PiD -->

---

## 📖 Introduction

**Latent Diffusion Models (LDMs)** are generative AI frameworks that perform the computationally heavy diffusion process inside a compressed "latent space" rather than raw pixel space. This vastly reduces computation requirements while maintaining high-fidelity generation. 🚀

<p align="center">
  <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExNHJmZnc4Y2R3N3N4OHB0ZTV4Z2x4Z2x4Z2x4Z2x4Z2x4Z2x4Z2x4JmVwPXYxX2ludGVybmFsX2dpZl9ieV9pZCZjdD1n/3o7TKVUn7iM8FMEU24/giphy.gif" alt="AI Diffusion Animation" width="400" />
</p>

## ✨ Key Features

- 🎨 **Multi-Modal Conditioning:** Text, Image, Layout, and Depth.
- ⚡ **Efficiency:** Low VRAM requirements via latent space processing.
- 🛠️ **Extensibility:** Compatible with ControlNet, LoRA, and IP-Adapter.
- 🧪 **Research Ready:** Includes foundational papers and recent breakthroughs.

---

## 🛠️ Categorized by Conditioning (Input Types)

LDMs adapt to user intent through several conditioning mechanisms that guide the generation process: 🧩

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
| **[Fast Decoders (e.g., PiD)](docs/pid.md)** | New paradigms replacing traditional autoencoder decoders with conditional pixel-space diffusion modules (Pixel Diffusion Decoder). | 2026 | [NVIDIA (PiD)](https://arxiv.org/abs/2605.23902) | [View Doc](docs/pid.md) |

## 📈 Star History
<div align="center">
   <a href="https://www.star-history.com/#ishandutta2007/Awesome-Latent-Diffusion-Models&Date">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=ishandutta2007/Awesome-Latent-Diffusion-Models&type=Date&theme=dark" />
      <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=ishandutta2007/Awesome-Latent-Diffusion-Models&type=Date" />
      <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=ishandutta2007/Awesome-Latent-Diffusion-Models&type=Date" />
    </picture>
   </a>
</div>

