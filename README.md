# GPT-SoVITS Colab Optimized

Optimized Google Colab notebook for running **GPT-SoVITS** (`v2Pro` / `v2ProPlus` & `v5turbo` / `v5dev`) on Tesla T4 (16 GB VRAM).

## Files

- `Colab_WebUI_Optimized.ipynb` (`v0.3.0`): FastBoot Colab notebook featuring:
  - Lightweight `condacolab.install()` (Miniconda instead of 1 GB Anaconda3).
  - Single-pass `PIP_CONSTRAINT` pinning (`torch==2.11.0+cu126`, `torchaudio==2.11.0+cu126`, `fastapi==0.115.12`, `starlette<0.47.0`).
  - Selective model download (`v2Pro + v5`, `v2Pro-only`, or `v5-only`), skipping legacy `v1`/`v2` and deprecated `v3`/`v4` weights.
  - Explicit `version` / `gpt_path` / `sovits_path` startup injection supporting `v2ProPlus`, `v2Pro`, `v5turbo`, and `v5dev`.
  - Google Drive workspace caching (`outputs`, `ref_audios`, `weights_backup`, `hf_cache`, optional `models_v2pro_cache`).
  - Compact single-card live HTML progress UI and per-stage timing summary.
  - Form-selectable launch modes (`inference_webui.py`, `inference_webui_fast.py`, `webui.py`, `tools/uvr5/webui.py`, `tools/subfix_webui.py`).

## Quick Start

1. Open [Google Colab](https://colab.research.google.com/) and upload `Colab_WebUI_Optimized.ipynb`.
2. Switch runtime to **T4 GPU** (`Runtime -> Change runtime type`).
3. Run **Step 1 -> Step 2A -> Step 2B -> Step 3** in order.
4. Click the generated `https://xxxx.gradio.live` link to open the TTS WebUI.
