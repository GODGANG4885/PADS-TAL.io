---
layout: project_page
permalink: /

title: PADS-TAL Padding Annealed Diffusion Sampling in Text Aligned Latent for Robust and Diverse Text-to-Music Generation
authors:
    anonymous
affiliations:
    anonymous
paper: https://www.cs.virginia.edu/~robins/Turing_Paper_1936.pdf
video: https://www.youtube.com/results?search_query=turing+machine
code: https://github.com/topics/turing-machines
data: https://huggingface.co/docs/datasets
---

<!-- Using HTML to center the abstract -->
<div class="columns is-centered has-text-centered">
    <div class="column is-four-fifths">
        <h2>Abstract</h2>
        <div class="content has-text-justified">
Text-to-Music (T2M) diffusion models increasingly adopt Transformer backbones (DiT), 
yet practical deployments often rely on short tag-style prompts and face persistent challenges: generations can collapse to limited patterns, while controlling diversity at inference time remains difficult under strict semantic requirements. Training-free sampling methods like CADS, while effective in Text-to-Image, can severely degrade alignment and fidelity in TTM because early-timestep perturbations strongly alter global musical attributes (e.g., genre, mood, structure). We propose two complementary solutions: Padding Annealed Diffusion Sampling (PADS), which injects timestep-dependent noise only into padding tokens while freezing semantic tokens to prevent semantic drift, and Text-Aligned Latent (TAL), a text-aware latent space learned via a redesigned VAE so diffusion sampling occurs near text-consistent neighborhoods. Together, PADS+TAL improve diversity while preserving prompt-aligned global attributes in TTM.
        </div>
    </div>
</div>

---
<div align="center">
<img src=static/image/Figure6.png alt="model">
</div>
---

## Audio Examples

### Task 1: [Text-to-Music]

<table>
  <tr>
    <th>Baseline</th>
    <th>CADS</th>
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
  <!-- <tr>
    <td colspan="3"><img src="assets/images/example_1_spec.png" alt="Spectrogram" style="width: 100%;"></td>
  </tr> -->
</table>

### Task 2: [Genre-based Music Generation]

<table>
  <tr>
    <th>Genre</th>
    <th>Baseline</th>
    <th>CADS</th>
    <th>Ours</th>
  </tr>

  <!-- Classic -->
  <tr>
    <td><b>Classic</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="assets/audio/reference_classic.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="assets/audio/reference_classic.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="assets/audio/baseline_classic.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="assets/audio/reference_classic.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="assets/audio/ours_classic.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="assets/audio/reference_classic.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>

  <!-- Pop -->
  <tr>
    <td><b>Pop</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="assets/audio/reference_pop.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="assets/audio/reference_classic.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="assets/audio/baseline_pop.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="assets/audio/reference_classic.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="assets/audio/ours_pop.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="assets/audio/reference_classic.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>

  <!-- Metal -->
  <tr>
    <td><b>Metal</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="assets/audio/reference_metal.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="assets/audio/reference_classic.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="assets/audio/baseline_metal.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="assets/audio/reference_classic.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="assets/audio/ours_metal.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="assets/audio/reference_classic.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
</table>

---



## Table: Comparison of Computable and Non-Computable Numbers

| Computable Numbers | Non-Computable Numbers |
|-------------------|-----------------------|
| Rational numbers, e.g., 1/2, 3/4 | Transcendental numbers, e.g., π, e |
| Algebraic numbers, e.g., √2, ∛3 | Non-algebraic numbers, e.g., √2 + √3 |
| Numbers with finite decimal representations | Numbers with infinite, non-repeating decimal representations |

He used the concept of a universal Turing machine to prove that the set of computable functions is recursively enumerable, meaning it can be listed by an algorithm.

## Significance
Turing's paper laid the foundation for the theory of computation and had a profound impact on the development of computer science. The Turing machine became a fundamental concept in theoretical computer science, serving as a theoretical model for studying the limits and capabilities of computation. Turing's work also influenced the development of programming languages, algorithms, and the design of modern computers.



[main]: static/image/Figure6.png