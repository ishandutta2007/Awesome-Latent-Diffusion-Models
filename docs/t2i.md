# Text-to-Image (T2I) Conditioning

Text-to-Image (T2I) is the most common conditioning method for Latent Diffusion Models, where a textual prompt is used to guide the generation of an image.

## Overview
In LDMs, the text prompt is typically encoded using a frozen text encoder (like CLIP or T5). The resulting embeddings are then cross-attended into the UNet layers during the denoising process.

## Diagram
<svg width="600" height="300" viewBox="0 0 600 300" xmlns="http://www.w3.org/2000/svg">
  <rect x="50" y="100" width="120" height="60" rx="10" fill="#4facfe" />
  <text x="110" y="135" font-family="Arial" font-size="14" fill="#fff" text-anchor="middle">Text Prompt</text>
  
  <rect x="220" y="100" width="120" height="60" rx="10" fill="#00f2fe" />
  <text x="280" y="135" font-family="Arial" font-size="14" fill="#fff" text-anchor="middle">Text Encoder</text>
  
  <rect x="390" y="100" width="160" height="100" rx="10" fill="#f093fb" />
  <text x="470" y="155" font-family="Arial" font-size="14" fill="#fff" text-anchor="middle">LDM Latent Space</text>
  
  <path d="M170 130 L220 130" stroke="#333" stroke-width="2" marker-end="url(#arrow)" />
  <path d="M340 130 L390 130" stroke="#333" stroke-width="2" marker-end="url(#arrow)" />
  
  <defs>
    <marker id="arrow" markerWidth="10" markerHeight="10" refX="0" refY="3" orient="auto" markerUnits="strokeWidth">
      <path d="M0,0 L0,6 L9,3 z" fill="#333" />
    </marker>
  </defs>
</svg>

## Technical Details
- **First Used:** 2021 (Rombach et al.)
- **Paper:** [High-Resolution Image Synthesis with Latent Diffusion Models](https://arxiv.org/abs/2112.10752)
- **Key Component:** Cross-attention mechanism between text embeddings and latent features.
