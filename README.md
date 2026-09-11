# LTX 2.5 FLF2V 8GB — Native Audio + Real Negative Prompt

This repository's current and recommended workflow is:

[`LTX_2.5_FLF2V_8GB_NATIVE_AUDIO_NEGATIVE.json`](./LTX_2.5_FLF2V_8GB_NATIVE_AUDIO_NEGATIVE.json)

The JSON is exported from the tested ComfyUI workflow and is the main version published in this repository.

## Features

- First Frame → Last Frame video generation
- Native LTX 2.5 audio generation
- Separate Visual Prompt
- Separate Native Audio Prompt
- Separate REAL Negative Prompt
- Negative conditioning connected directly to the guider
- Designed and tested for 8 GB VRAM
- Adjustable resolution, duration and FPS
- ComfyUI workflow ready to import

The workflow uses the native LTX 2.5 audio path and includes visible controls for `VISUAL PROMPT`, `AUDIO PROMPT`, and `NEGATIVE PROMPT`. The negative text is encoded through `CLIPTextEncode` and reaches the negative conditioning input of `LTXV Dual CFG Guider`.

## Models

The workflow references these LTX 2.5 8 GB model files:

- `ltx-2.5-22b-distilled-transformer-w4a8_convrot.safetensors`
- `gemma4-12b-with-proj-ltx-2.5-w4a8_convrot.safetensors` (Gemma 4 12B with LTX 2.5 projection)
- `ltx-2.5-video-vae-bf16.safetensors`
- `ltx-2.5-audio-vae-bf16.safetensors`

Place them in the corresponding ComfyUI model directories, such as `models/diffusion_models`, `models/text_encoders`, and `models/vae`.

## VRAM warning

This workflow is specifically designed for GPUs with 8 GB of VRAM. Actual memory usage can vary depending on the selected resolution, clip duration, loaded models, and ComfyUI configuration. Lower the resolution or duration if the available VRAM is insufficient.

## Import

Import the JSON into ComfyUI, load the desired First Frame and Last Frame images, then adjust the visible prompt, resolution, duration, FPS, and native audio controls as needed.

This repository intentionally publishes this FLF2V Native Audio + Real Negative Prompt workflow as its main version. It is not a Motion, LoRA, or Director workflow.
