# Spatial/Depth-to-Image

Spatial conditioning uses physical geometry maps, such as depth maps or edge maps (Canny), to guide image generation.

## Overview
This method ensures that the generated image adheres to the structure of the input geometry. It's widely used in architectural visualization and character posing.

## Diagram
<svg width="600" height="300" viewBox="0 0 600 300" xmlns="http://www.w3.org/2000/svg">
  <path d="M50 150 L100 50 L150 150 Z" fill="#ccc" stroke="#333" />
  <text x="100" y="165" font-family="Arial" font-size="12" fill="#333" text-anchor="middle">Depth Map</text>
  
  <rect x="220" y="100" width="120" height="60" rx="10" fill="#84fab0" />
  <text x="280" y="135" font-family="Arial" font-size="14" fill="#333" text-anchor="middle">ControlNet / Adapter</text>
  
  <rect x="390" y="100" width="160" height="100" rx="10" fill="#f093fb" />
  <text x="470" y="155" font-family="Arial" font-size="14" fill="#fff" text-anchor="middle">LDM UNet</text>
  
  <path d="M150 100 L220 130" stroke="#333" stroke-width="2" marker-end="url(#arrow)" />
  <path d="M340 130 L390 130" stroke="#333" stroke-width="2" marker-end="url(#arrow)" />
  
  <defs>
    <marker id="arrow" markerWidth="10" markerHeight="10" refX="0" refY="3" orient="auto" markerUnits="strokeWidth">
      <path d="M0,0 L0,6 L9,3 z" fill="#333" />
    </marker>
  </defs>
</svg>

## Technical Details
- **First Used:** 2021 (Rombach et al.) / Popularized by ControlNet (2023)
- **Paper:** [High-Resolution Image Synthesis with Latent Diffusion Models](https://arxiv.org/abs/2112.10752)
- **Key Feature:** Maintains structural integrity while allowing for creative style changes.
