# Inpainting & Outpainting

Inpainting and Outpainting are specialized tasks for modifying specific parts of an image or extending its borders.

## Overview
- **Inpainting:** The model fills in a masked area of an image based on the surrounding context and an optional text prompt.
- **Outpainting:** The model generates content beyond the original boundaries of the image, maintaining stylistic and structural consistency.

## Diagram
<svg width="600" height="300" viewBox="0 0 600 300" xmlns="http://www.w3.org/2000/svg">
  <rect x="50" y="50" width="150" height="150" fill="#dfe6e9" stroke="#333" />
  <rect x="90" y="90" width="70" height="70" fill="#2d3436" />
  <text x="125" y="125" font-family="Arial" font-size="10" fill="#fff" text-anchor="middle">Mask</text>
  
  <path d="M220 125 L300 125" stroke="#333" stroke-width="2" marker-end="url(#arrow)" />
  
  <rect x="350" y="50" width="150" height="150" fill="#dfe6e9" stroke="#333" />
  <circle cx="425" cy="125" r="30" fill="#fab1a0" />
  <text x="425" y="125" font-family="Arial" font-size="10" fill="#333" text-anchor="middle">Generated Content</text>
  
  <defs>
    <marker id="arrow" markerWidth="10" markerHeight="10" refX="0" refY="3" orient="auto" markerUnits="strokeWidth">
      <path d="M0,0 L0,6 L9,3 z" fill="#333" />
    </marker>
  </defs>
</svg>

## Technical Details
- **First Used:** 2021 (Rombach et al.)
- **Paper:** [High-Resolution Image Synthesis with Latent Diffusion Models](https://arxiv.org/abs/2112.10752)
- **Technique:** Concatenating the mask and the masked image latents to the input.
