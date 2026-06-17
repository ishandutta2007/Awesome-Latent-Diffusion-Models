# Image-to-Image (I2I) Transformation

Image-to-Image (I2I) conditioning allows for modifying an existing image while preserving its underlying structure and composition.

## Overview
The source image is first encoded into the latent space. Denoising then starts from this noisy latent representation, guided by a text prompt to perform transformations.

## Diagram
<svg width="600" height="300" viewBox="0 0 600 300" xmlns="http://www.w3.org/2000/svg">
  <rect x="50" y="50" width="100" height="100" rx="5" fill="#a1c4fd" />
  <text x="100" y="105" font-family="Arial" font-size="12" fill="#333" text-anchor="middle">Source Image</text>
  
  <rect x="200" y="100" width="120" height="60" rx="10" fill="#c2e9fb" />
  <text x="260" y="135" font-family="Arial" font-size="14" fill="#333" text-anchor="middle">Encoder + Noise</text>
  
  <rect x="370" y="100" width="180" height="100" rx="10" fill="#f093fb" />
  <text x="460" y="155" font-family="Arial" font-size="14" fill="#fff" text-anchor="middle">Diffusion Reverse</text>
  
  <path d="M150 100 L200 130" stroke="#333" stroke-width="2" marker-end="url(#arrow)" />
  <path d="M320 130 L370 130" stroke="#333" stroke-width="2" marker-end="url(#arrow)" />
  
  <defs>
    <marker id="arrow" markerWidth="10" markerHeight="10" refX="0" refY="3" orient="auto" markerUnits="strokeWidth">
      <path d="M0,0 L0,6 L9,3 z" fill="#333" />
    </marker>
  </defs>
</svg>

## Technical Details
- **First Used:** 2021 (Rombach et al.)
- **Paper:** [High-Resolution Image Synthesis with Latent Diffusion Models](https://arxiv.org/abs/2112.10752)
- **Key Parameter:** Denoising strength (determines how much of the original image is preserved).
