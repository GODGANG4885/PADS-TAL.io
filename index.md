---
layout: default
title: Your Project Title
---

<div align="center">

# PADS-TAL : Padding Annealed Diffusion Sampling in Text Aligned Latent for Robust and Diverse Text-to-Music Generation
## 

**Author Name<sup>1,2*</sup>, Co-Author Name<sup>1</sup>, Another Author<sup>2</sup>**

<sup>1</sup>Your University or Institution  
<sup>2</sup>Affiliated Company or Lab  
<sup>*</sup>Equal contribution or corresponding author

[Paper](https://arxiv.org/abs/your-paper-id) | [Code](https://github.com/your-username/your-repo) | [Demo](https://huggingface.co/your-demo) | [🤗 HF Demo](https://huggingface.co/spaces/your-space)

</div>

---

## Abstract

Text-to-Music (T2M) diffusion models increasingly adopt Transformer backbones (DiT), 
yet practical deployments often rely on short tag-style prompts and face persistent challenges: generations can collapse to limited patterns, while controlling diversity at inference time remains difficult under strict semantic requirements. Training-free sampling methods like CADS, while effective in Text-to-Image, can severely degrade alignment and fidelity in TTM because early-timestep perturbations strongly alter global musical attributes (e.g., genre, mood, structure). We propose two complementary solutions: Padding Annealed Diffusion Sampling (PADS), which injects timestep-dependent noise only into padding tokens while freezing semantic tokens to prevent semantic drift, and Text-Aligned Latent (TAL), a text-aware latent space learned via a redesigned VAE so diffusion sampling occurs near text-consistent neighborhoods. Together, PADS+TAL improve diversity while preserving prompt-aligned global attributes in TTM.

---

## Method Overview

![Method Overview](assets/images/method_overview.png)
*Figure 1: Overview of our proposed method.*

### Key Contributions

1. **Contribution 1**: Detailed explanation
2. **Contribution 2**: Detailed explanation
3. **Contribution 3**: Detailed explanation

---

## Results

### Quantitative Results

| Method | CLAP Score ↑ | Other Metric ↑ | Speed ↓ |
|--------|--------------|----------------|---------|
| Baseline | 0.30 | - | - |
| Method A | 0.32 | - | - |
| Method B | 0.34 | - | - |
| **Ours** | **0.36** | **-** | **-** |

### Qualitative Results

![Results Visualization](assets/images/evaluation_results_plot.png)
*Figure 2: Performance comparison across different configurations.*

---

## Audio Examples

### Task 1: [Description]

<table>
  <tr>
    <th>Reference</th>
    <th>Baseline</th>
    <th>Ours</th>
  </tr>
  <tr>
    <td>
      <audio controls style="width: 200px;">
        <source src="assets/audio/reference_1.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="assets/audio/baseline_1.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="assets/audio/ours_1.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td colspan="3"><img src="assets/images/example_1_spec.png" alt="Spectrogram" style="width: 100%;"></td>
  </tr>
</table>

### Task 2: [Description]

<table>
  <tr>
    <th>Reference</th>
    <th>Baseline</th>
    <th>Ours</th>
  </tr>
  <tr>
    <td>
      <audio controls style="width: 200px;">
        <source src="assets/audio/reference_2.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="assets/audio/baseline_2.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="assets/audio/ours_2.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td colspan="3"><img src="assets/images/example_2_spec.png" alt="Spectrogram" style="width: 100%;"></td>
  </tr>
</table>

---

## Additional Results

### Ablation Studies

![Ablation Studies](assets/images/ablation_plot.png)
*Figure 3: Ablation study results showing the impact of different components.*

### Parameter Analysis

![Parameter Analysis](assets/images/scheduler_plot.png)
*Figure 4: Analysis of different parameter configurations.*

---

## BibTeX

If you find this work useful, please cite:

```bibtex
@inproceedings{yourname2024yourmethod,
    title={Your Method: Full Title Here},
    author={Your Name and Co-Author Name and Another Author},
    booktitle={Conference Name (Acronym)},
    year={2024}
}
```

---

## Acknowledgements

We thank [people/organizations] for [contributions]. This work was supported by [funding sources].

Special thanks to:
- [Person/Lab] for [contribution]
- [Tool/Resource] for [usage]

---

## Contact

For questions or collaborations, please contact:
- **First Author**: [email@domain.com](mailto:email@domain.com)
- **Project Page**: [https://your-username.github.io/project-name](https://your-username.github.io/project-name)
- **GitHub**: [https://github.com/your-username/project-name](https://github.com/your-username/project-name)

<style>
  body {
    font-family: "Times", "DejaVu Serif", serif;
    line-height: 1.6;
    max-width: 900px;
    margin: 0 auto;
    padding: 20px;
  }
  h1, h2, h3 {
    font-weight: bold;
  }
  table {
    margin: 20px auto;
    border-collapse: collapse;
  }
  th, td {
    padding: 10px;
    text-align: center;
    border: 1px solid #ddd;
  }
  th {
    background-color: #f2f2f2;
    font-weight: bold;
  }
  img {
    max-width: 100%;
    height: auto;
    display: block;
    margin: 10px auto;
  }
  audio {
    display: block;
    margin: 10px auto;
  }
  code {
    background-color: #f5f5f5;
    padding: 2px 4px;
    border-radius: 3px;
  }
  pre {
    background-color: #f5f5f5;
    padding: 15px;
    border-radius: 5px;
    overflow-x: auto;
  }
</style>

