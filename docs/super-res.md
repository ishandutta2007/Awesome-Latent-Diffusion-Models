# Super-Resolution / Denoising

Super-Resolution (SR) in LDMs involves decoding low-resolution latent representations into high-resolution outputs by predicting and synthesizing missing spatial details.

## Overview
LDMs are inherently suited for SR because they can learn to map coarse features to fine details during the denoising process. This is often used as a final stage in a generation pipeline.

## Diagram
<svg width="600" height="300" viewBox="0 0 600 300" xmlns="http://www.w3.org/2000/svg">
  <rect x="50" y="120" width="40" height="40" fill="#a1c4fd" stroke="#333" />
  <text x="70" y="175" font-family="Arial" font-size="10" fill="#333" text-anchor="middle">Low-Res Latent</text>
  
  <path d="M110 140 L200 140" stroke="#333" stroke-width="2" marker-end="url(#arrow)" />
  
  <rect x="250" y="50" width="200" height="200" fill="#c2e9fb" stroke="#333" />
  <text x="350" y="270" font-family="Arial" font-size="12" fill="#333" text-anchor="middle">High-Res Output</text>
  
  <defs>
    <marker id="arrow" markerWidth="10" markerHeight="10" refX="0" refY="3" orient="auto" markerUnits="strokeWidth">
      <path d="M0,0 L0,6 L9,3 z" fill="#333" />
    </marker>
  </defs>
</svg>

## Technical Details
- **First Used:** 2021 (Rombach et al.)
- **Paper:** [High-Resolution Image Synthesis with Latent Diffusion Models](https://arxiv.org/abs/2112.10752)
- **Key Advantage:** Significant reduction in VRAM compared to pixel-space SR.
