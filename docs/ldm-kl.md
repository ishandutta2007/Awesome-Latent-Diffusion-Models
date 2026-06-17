# LDM-KL (Kullback-Leibler)

LDM-KL models utilize Kullback-Leibler (KL) regularization during the autoencoding phase to ensure a smooth and continuous latent distribution.

## Overview
By penalizing the deviation of the latent distribution from a standard normal distribution, LDM-KL produces a latent space that is better suited for continuous diffusion processes. This is the standard approach for models like Stable Diffusion.

## Diagram
<svg width="600" height="300" viewBox="0 0 600 300" xmlns="http://www.w3.org/2000/svg">
  <rect x="50" y="100" width="100" height="60" rx="5" fill="#84fab0" />
  <text x="100" y="135" font-family="Arial" font-size="12" fill="#333" text-anchor="middle">Encoder</text>
  
  <ellipse cx="260" cy="130" rx="60" ry="40" fill="rgba(143, 211, 244, 0.5)" stroke="#2d3436" stroke-dasharray="5,5" />
  <text x="260" y="135" font-family="Arial" font-size="12" fill="#333" text-anchor="middle">KL-Regularized Space</text>
  
  <rect x="370" y="100" width="180" height="60" rx="5" fill="#f093fb" />
  <text x="460" y="135" font-family="Arial" font-size="12" fill="#fff" text-anchor="middle">Continuous Latent</text>
  
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
- **Key Benefit:** Smooth latent interpolation and stable training.
