# Fast Decoders (PiD)

PiD (Pixel diffusion Decoder) replaces traditional VAE decoders with conditional pixel-space diffusion modules for high-resolution synthesis.

## Overview
Traditional VAE decoders often lose detail during reconstruction. PiD treats decoding as a generative diffusion task in pixel space, allowing for ultra-fast and high-fidelity upscaling to megapixel resolutions.

## Diagram
<svg width="600" height="300" viewBox="0 0 600 300" xmlns="http://www.w3.org/2000/svg">
  <rect x="50" y="120" width="60" height="60" rx="5" fill="#a18cd1" />
  <text x="80" y="195" font-family="Arial" font-size="10" fill="#333" text-anchor="middle">Latent</text>
  
  <path d="M110 150 L200 150" stroke="#333" stroke-width="2" marker-end="url(#arrow)" />
  
  <rect x="250" y="100" width="120" height="100" rx="10" fill="#fbc2eb" />
  <text x="310" y="155" font-family="Arial" font-size="14" fill="#333" text-anchor="middle">PiD (4 Steps)</text>
  
  <path d="M370 150 L450 150" stroke="#333" stroke-width="2" marker-end="url(#arrow)" />
  
  <rect x="470" y="50" width="100" height="200" fill="#84fab0" stroke="#333" />
  <text x="520" y="270" font-family="Arial" font-size="12" fill="#333" text-anchor="middle">2K Image</text>
  
  <defs>
    <marker id="arrow" markerWidth="10" markerHeight="10" refX="0" refY="3" orient="auto" markerUnits="strokeWidth">
      <path d="M0,0 L0,6 L9,3 z" fill="#333" />
    </marker>
  </defs>
</svg>

## Technical Details
- **First Used:** 2026 (NVIDIA)
- **Paper:** [PiD: Fast and High-Resolution Latent Decoding with Pixel Diffusion](https://arxiv.org/abs/2605.23902)
- **Performance:** <1s for 2K images on RTX 5090.
