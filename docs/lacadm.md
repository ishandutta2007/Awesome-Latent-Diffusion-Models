# Latent Causal Diffusion Models (LacaDM)

LacaDM integrates structural causal models with Latent Diffusion Models to enable precise causal interventions and counterfactual reasoning.

## Overview
Unlike standard LDMs that learn aesthetic correlations, LacaDM learns the underlying causal relationships between environmental states and policies, making it ideal for Reinforcement Learning and Scientific Discovery.

## Diagram
<svg width="600" height="300" viewBox="0 0 600 300" xmlns="http://www.w3.org/2000/svg">
  <circle cx="100" cy="100" r="30" fill="#ff9a9e" stroke="#333" />
  <text x="100" y="105" font-family="Arial" font-size="12" fill="#333" text-anchor="middle">Cause A</text>
  
  <circle cx="250" cy="100" r="30" fill="#fad0c4" stroke="#333" />
  <text x="250" y="105" font-family="Arial" font-size="12" fill="#333" text-anchor="middle">Effect B</text>
  
  <path d="M130 100 L220 100" stroke="#333" stroke-width="2" marker-end="url(#arrow)" />
  
  <rect x="350" y="70" width="180" height="100" rx="10" fill="#fbc2eb" />
  <text x="440" y="125" font-family="Arial" font-size="14" fill="#333" text-anchor="middle">Causal Latent Space</text>
  
  <defs>
    <marker id="arrow" markerWidth="10" markerHeight="10" refX="0" refY="3" orient="auto" markerUnits="strokeWidth">
      <path d="M0,0 L0,6 L9,3 z" fill="#333" />
    </marker>
  </defs>
</svg>

## Technical Details
- **First Used:** 2025 (Zhang et al.)
- **Paper:** [LacaDM: A Latent Causal Diffusion Model for Multiobjective Reinforcement Learning](https://arxiv.org/abs/2512.19516)
- **Application:** Multi-objective RL, Causal representation learning.
