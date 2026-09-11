# LTX 2.5 FLF2V 8GB — Native Audio + Real Negative Prompt

El workflow actual y recomendado de este repositorio es:

[`LTX_2.5_FLF2V_8GB_NATIVE_AUDIO_NEGATIVE.json`](./LTX_2.5_FLF2V_8GB_NATIVE_AUDIO_NEGATIVE.json)

El JSON está exportado desde el workflow probado en ComfyUI y es la versión principal publicada en este repositorio.

## Características

- Generación de vídeo desde First Frame → Last Frame
- Generación de audio nativo de LTX 2.5
- Visual Prompt separado
- Native Audio Prompt separado
- REAL Negative Prompt separado
- El negative conditioning está conectado directamente al guider
- Diseñado y probado para 8 GB de VRAM
- Resolución, duración y FPS ajustables
- Workflow de ComfyUI listo para importar

El workflow utiliza la ruta de audio nativo de LTX 2.5 e incluye controles visibles para `VISUAL PROMPT`, `AUDIO PROMPT` y `NEGATIVE PROMPT`. El texto negativo pasa por `CLIPTextEncode` y llega a la entrada de conditioning negativo de `LTXV Dual CFG Guider`.

## Modelos

El workflow referencia estos archivos de modelos LTX 2.5 para 8 GB:

- `ltx-2.5-22b-distilled-transformer-w4a8_convrot.safetensors`
- `gemma4-12b-with-proj-ltx-2.5-w4a8_convrot.safetensors` (Gemma 4 12B con proyección LTX 2.5)
- `ltx-2.5-video-vae-bf16.safetensors`
- `ltx-2.5-audio-vae-bf16.safetensors`

Colócalos en las carpetas correspondientes de modelos de ComfyUI, como `models/diffusion_models`, `models/text_encoders` y `models/vae`.

## Advertencia de VRAM

Este workflow está diseñado específicamente para GPUs con 8 GB de VRAM. El consumo real puede variar según la resolución elegida, la duración del clip, los modelos cargados y la configuración de ComfyUI. Reduce la resolución o la duración si la VRAM disponible no es suficiente.

## Importación

Importa el JSON en ComfyUI, carga las imágenes deseadas de First Frame y Last Frame y ajusta los prompts visibles, la resolución, la duración, los FPS y los controles de audio nativo según necesites.

Este repositorio publica intencionadamente este workflow FLF2V Native Audio + Real Negative Prompt como su versión principal. No es un workflow Motion, LoRA ni Director.
