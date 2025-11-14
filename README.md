# Improving Pronunciation in Conditional Flow Matching Neural TTS Models (Ongoing)

This repository will host the development and experiments aimed at improving the pronunciation accuracy of **Conditional Flow Matching (CFM)** neural text-to-speech (TTS) models. The project is part of a research collaboration between [LIUM](https://lium.univ-lemans.fr/) and [Voxygen](https://www.voxygen.fr/home).

## Project Overview

The goal of this project is to enhance the robustness and pronunciation quality of neural TTS models by:  

- Training a Conditional Flow Matching TTS system on the **Blizzard Challenge 2023** dataset.  
- Evaluating the output with a speech recognition model to measure pronunciation accuracy.  
- Investigating the impact of text-acoustic alignment in conditioning the TTS model.  
- Applying reinforcement learning to reduce transcription errors and improve robustness across speakers and languages.  


## Concrete steps to apply
- Segment and preprocess the [Blizzard2023](https://zenodo.org/records/7560290) dataset, converting long-form audio into segmented clips based on the metadata.
- Run inference with the Conditional Flow Matching model [ZipVoice](https://github.com/k2-fsa/ZipVoice) to generate synthetic audio from the dataset.
- Use [tts4all_eval](https://git-lium.univ-lemans.fr/jsalt2025/wp1/tts4all_eval) to assess the quality of the synthetic audio by comparing it with the reference dataset using Character Error Rate (CER) and Word Error Rate (WER).
- Finetune [ZipVoice](https://github.com/k2-fsa/ZipVoice), pre-trained on the [Emilia dataset](https://huggingface.co/datasets/amphion/Emilia-Dataset), on the **Blizzard2023** dataset to improve generation quality.
- Finetune [Whisper-Large-v3](https://huggingface.co/openai/whisper-large-v3), used for transcribing audio into text, on **Blizzard2023** to improve performance.
- **More steps and code to come**

