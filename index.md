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


<div align="center">
<img src=static/image/Figure11.png alt="model">
</div>


## Audio Examples

### Task 1: [Text-to-Music with Random Prompts]

#### Input Prompt 1: jazz, piano trio, swing, live recording feel, warm tone, improvisation

<table>
  <tr>
    <th>Sample</th>
    <th>Baseline</th>
    <th>Ours (PADS)</th>
  </tr>
  <tr>
    <td><b>Sample 1</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/task1/1114_0.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/task1/1114_0.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>Sample 2</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/task1/1114_1.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/task1/1114_1.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>Sample 3</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/task1/1114_2.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/task1/1114_2.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>Sample 4</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/task1/1114_3.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/task1/1114_3.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
</table>

#### Input Prompt 2: lofi, chill, vinyl noise, mellow, soft drums, warm chords, nostalgic

<table>
  <tr>
    <th>Sample</th>
    <th>Baseline</th>
    <th>Ours (PADS)</th>
  </tr>
  <tr>
    <td><b>Sample 1</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/task1/1115_0.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/task1/1115_0.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>Sample 2</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/task1/1115_1.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/task1/1115_1.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>Sample 3</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/task1/1115_2.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/task1/1115_2.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>Sample 4</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/task1/1115_3.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/task1/1115_3.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
</table>

#### Input Prompt 3: soundtrack, underscore, tension, subtle strings, low dynamics, cinematic

<table>
  <tr>
    <th>Sample</th>
    <th>Baseline</th>
    <th>Ours (PADS)</th>
  </tr>
  <tr>
    <td><b>Sample 1</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/task1/1118_0.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/task1/1118_1.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>Sample 2</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/task1/1118_1.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/task1/1118_2.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>Sample 3</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/task1/1118_2.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/task1/1118_3.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
  <tr>
    <td><b>Sample 4</b></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/task1/1118_3.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/task1/1118_1.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>
</table>

### Task 2: [Genre-based Music Generation]

<table>
  <tr>
    <th>Genre</th>
    <th>Baseline</th>
    <th>CADS</th>
    <th>Ours</th>
  </tr>

  <!-- Tropical House -->
  <tr>
    <td><b>Tropical House</b><br><i style="font-size: 0.85em; color: #666;">electric piano, synthesizer, tropical house, energy, digital processing capabilities, 105 bpm</i></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/tropical/121_0.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/tropical/121_1.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/tropical/121_2.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/tropical/121_3.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/cads/tropical/121_0.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/cads/tropical/121_1.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/cads/tropical/121_2.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/cads/tropical/121_3.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/tropical/121_0.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/tropical/121_1.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/tropical/121_2.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/tropical/121_3.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>

  <!-- Jazz -->
  <tr>
    <td><b>Jazz</b><br><i style="font-size: 0.85em; color: #666;">jazz</i></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/jazz/0_0.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/jazz/0_1.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/jazz/0_2.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/cads/jazz/0_0.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/cads/jazz/0_1.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/cads/jazz/0_2.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/jazz/0_0.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/jazz/0_1.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/jazz/0_2.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>

  <!-- Acoustic -->
  <tr>
    <td><b>Acoustic</b><br><i style="font-size: 0.85em; color: #666;">slide guitar, piano, 125 bpm, plucked string instrument, strings, acoustic, mellow, musical instrument</i></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/accoustic/317_0.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/accoustic/317_1.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/accoustic/317_2.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/accoustic/317_3.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/cads/accoustic/317_0.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/cads/accoustic/317_1.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/cads/accoustic/317_2.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/cads/accoustic/317_3.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/accoustic/317_0.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/accoustic/317_1.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/accoustic/317_2.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/accoustic/317_3.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>

  <!-- Carol -->
  <tr>
    <td><b>Carol</b><br><i style="font-size: 0.85em; color: #666;">guitar, ambient, bass, 100 bpm, ding, glockenspiel, moving, tinkle, jingle, mellow, carol, chill, relaxing</i></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/carol/37_0.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/carol/37_1.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/carol/37_2.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/carol/37_3.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/cads/carol/37_0.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/cads/carol/37_1.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/cads/carol/37_2.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/cads/carol/37_3.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/carol/37_0.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/carol/37_1.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/carol/37_2.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/carol/37_3.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>

  <!-- Electronic Pop -->
  <tr>
    <td><b>Electronic Pop</b><br><i style="font-size: 0.85em; color: #666;">guitar, electronic dance music, musical instrument, rhythmical, piano</i></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/elecpop/244_0.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/elecpop/244_1.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/elecpop/244_2.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/elecpop/244_3.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/cads/elecpop/244_0.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/cads/elecpop/244_1.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/cads/elecpop/244_2.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/cads/elecpop/244_3.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/elecpop/244_0.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/elecpop/244_1.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/elecpop/244_2.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/elecpop/244_3.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>

  <!-- Electronic -->
  <tr>
    <td><b>Electronic</b><br><i style="font-size: 0.85em; color: #666;">ambient, 125 bpm, dubstep, bouncy, drum kit, electronic dance music, drum machine, electronic, sampler</i></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/electronic/91_0.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/electronic/91_1.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/electronic/91_2.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/electronic/91_3.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/cads/electronic/91_0.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/cads/electronic/91_1.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/cads/electronic/91_2.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/cads/electronic/91_3.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/electronic/91_0.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/electronic/91_1.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/electronic/91_2.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/electronic/91_3.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>

  <!-- New Age -->
  <tr>
    <td><b>New Age</b><br><i style="font-size: 0.85em; color: #666;">115 bpm, piano, synthesizer, new-age music, cello, soft, electric piano</i></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/newage/181_0.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/newage/181_1.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/newage/181_2.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/newage/181_3.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/cads/newage/181_0.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/cads/newage/181_1.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/cads/newage/181_2.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/cads/newage/181_3.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/newage/181_0.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/newage/181_1.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/newage/181_2.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/newage/181_3.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
  </tr>

  <!-- Pop -->
  <tr>
    <td><b>Pop</b><br><i style="font-size: 0.85em; color: #666;">pop, ambient, 110 bpm, drums, piano, pink noise, chill</i></td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/pop/277_0.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/pop/277_1.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/pop/277_2.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/stable_audio/baseline/pop/277_3.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/cads/pop/277_0.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/cads/pop/277_1.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/cads/pop/277_2.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/cads/pop/277_3.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </td>
    <td>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/pop/277_0.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/pop/277_1.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/pop/277_2.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
      <audio controls style="width: 200px;">
        <source src="static/audio_samples/TAL/pads/pop/277_3.wav" type="audio/wav">
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





[main]: static/image/Figure6.png