# LDM-VQ (Vector Quantized)

LDM-VQ models utilize Vector Quantization (VQ) in the autoencoder stage to represent images as a discrete set of latent codes.

## Overview
Based on the VQ-GAN architecture, the encoder maps images to a discrete codebook. This is particularly useful for categorical image synthesis and handling discrete structures within the latent space.

## Diagram
<svg width="600" height="300" viewBox="0 0 600 300" xmlns="http://www.w3.org/2000/svg">
  <rect x="50" y="100" width="100" height="60" rx="5" fill="#fbc2eb" />
  <text x="100" y="135" font-family="Arial" font-size="12" fill="#333" text-anchor="middle">Encoder</text>
  
  <rect x="200" y="80" width="120" height="100" rx="5" fill="#a6c1ee" />
  <text x="260" y="120" font-family="Arial" font-size="12" font-weight="bold" fill="#333" text-anchor="middle">Codebook</text>
  <rect x="220" y="135" width="20" height="20" fill="#fff" stroke="#333" />
  <rect x="250" y="135" width="20" height="20" fill="#fff" stroke="#333" />
  <rect x="280" y="135" width="20" height="20" fill="#fff" stroke="#333" />
  
  <rect x="370" y="100" width="180" height="60" rx="5" fill="#f093fb" />
  <text x="460" y="135" font-family="Arial" font-size="12" fill="#fff" text-anchor="middle">Quantized Latent</text>
  
  <path d="M150 130 L200 130" stroke="#333" stroke-width="2" marker-end="url(#arrow)" />
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
- **Base Model:** VQ-REG / VQ-GAN.
