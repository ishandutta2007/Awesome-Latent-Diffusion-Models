# Stable Diffusion

Stable Diffusion is the most widely recognized open-source implementation of Latent Diffusion Models, developed by CompVis, Stability AI, and LAION.

## Overview
It utilizes a VAE for image compression, a UNet for the diffusion process in latent space, and a CLIP text encoder for conditioning. Recent versions like SDXL and SD3 have introduced significant improvements in resolution and prompt adherence.

## Diagram
<svg width="600" height="300" viewBox="0 0 600 300" xmlns="http://www.w3.org/2000/svg">
  <rect x="20" y="100" width="100" height="60" rx="5" fill="#8ec5fc" />
  <text x="70" y="135" font-family="Arial" font-size="12" fill="#333" text-anchor="middle">VAE Encoder</text>
  
  <rect x="150" y="50" width="300" height="200" rx="10" fill="#e0c3fc" stroke="#333" />
  <text x="300" y="80" font-family="Arial" font-size="16" font-weight="bold" fill="#333" text-anchor="middle">Latent Space (UNet)</text>
  <path d="M200 120 L400 180 M200 180 L400 120" stroke="rgba(0,0,0,0.2)" />
  
  <rect x="480" y="100" width="100" height="60" rx="5" fill="#8ec5fc" />
  <text x="530" y="135" font-family="Arial" font-size="12" fill="#333" text-anchor="middle">VAE Decoder</text>
  
  <path d="M120 130 L150 130" stroke="#333" stroke-width="2" marker-end="url(#arrow)" />
  <path d="M450 130 L480 130" stroke="#333" stroke-width="2" marker-end="url(#arrow)" />
  
  <defs>
    <marker id="arrow" markerWidth="10" markerHeight="10" refX="0" refY="3" orient="auto" markerUnits="strokeWidth">
      <path d="M0,0 L0,6 L9,3 z" fill="#333" />
    </marker>
  </defs>
</svg>

## Technical Details
- **First Used:** 2021 (Architecture) / 2022 (Public Release)
- **Paper:** [High-Resolution Image Synthesis with Latent Diffusion Models](https://arxiv.org/abs/2112.10752)
- **Variants:** SD 1.5, SD 2.1, SDXL, SD3, SVD.
