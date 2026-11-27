# GPT-SoVITS Colab Optimized

Optimized Google Colab notebook for running **GPT-SoVITS** on Tesla T4 (16 GB VRAM).

## Files

- `Colab_WebUI_Optimized.ipynb`: Pre-configured Colab notebook featuring:
  - Pinned compatibility fixes (`torch==2.11.0+cu126`, `torchaudio==2.11.0+cu126`, `fastapi==0.115.12`, `starlette<0.47.0`).
  - Google Drive workspace caching (`outputs`, `ref_audios`, `weights_backup`, `hf_cache`).
  - Live HTML progress bar and per-stage execution timing.
  - Form-selectable launch modes (`inference_webui.py`, `inference_webui_fast.py`, `webui.py`, `tools/uvr5/webui.py`, `tools/subfix_webui.py`), defaulting to `inference_webui.py zh_CN`.

## Quick Start

1. Open [Google Colab](https://colab.research.google.com/) and upload `Colab_WebUI_Optimized.ipynb`.
2. Switch runtime to **T4 GPU** (`Runtime -> Change runtime type`).
3. Run **Step 1 -> Step 2A -> Step 2B -> Step 3** in order.
4. Click the generated `https://xxxx.gradio.live` link to open the TTS WebUI.
