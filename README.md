# ai-models

Copies of the open models our apps download, so a download never depends on a single
third-party host. Every file is a **byte-identical copy** of a pinned upstream revision; the
apps check each one against the SHA-256 below and reject anything else.

Files are attached to [releases](../../releases), one release per model:
`https://github.com/nhrclk/ai-models/releases/download/<tag>/<file>`.

| Tag | Model | Files | Licence |
|---|---|---|---|
| `whisperTurbo-1` | Whisper large-v3-turbo, GGML Q8_0 (OpenAI, via whisper.cpp) | `ggml-large-v3-turbo-q8_0.bin` | MIT |
| `parakeet-1` | Parakeet TDT 0.6B v3, int8 ONNX (NVIDIA, export by sherpa-onnx) | `encoder.int8.onnx`, `decoder.int8.onnx`, `joiner.int8.onnx`, `tokens.txt` | CC-BY-4.0 |
| `hyMt2-1` | Hy-MT2 1.8B, GGUF Q4_K_M (Tencent) | `Hy-MT2-1.8B-Q4_K_M.gguf` | Apache-2.0 |
| `openVoice-1` | OpenVoice V2 tone-colour converter, ONNX fp32 (MyShell) | `openvoice_v2_tone_color_converter.onnx` | MIT |

## Sources and checksums

| File | Bytes | SHA-256 | Copied from |
|---|---|---|---|
| `ggml-large-v3-turbo-q8_0.bin` | 874188075 | `317eb69c11673c9de1e1f0d459b253999804ec71ac4c23c17ecf5fbe24e259a1` | [ggerganov/whisper.cpp @ 5359861](https://huggingface.co/ggerganov/whisper.cpp/tree/5359861c739e955e79d9a303bcbc70fb988958b1) |
| `encoder.int8.onnx` | 652184281 | `acfc2b4456377e15d04f0243af540b7fe7c992f8d898d751cf134c3a55fd2247` | [csukuangfj/sherpa-onnx-nemo-parakeet-tdt-0.6b-v3-int8 @ 2bda32e](https://huggingface.co/csukuangfj/sherpa-onnx-nemo-parakeet-tdt-0.6b-v3-int8/tree/2bda32ec70b097a55adaa07d9a7173915b43cc78) |
| `decoder.int8.onnx` | 11845275 | `179e50c43d1a9de79c8a24149a2f9bac6eb5981823f2a2ed88d655b24248db4e` | same |
| `joiner.int8.onnx` | 6355277 | `3164c13fc2821009440d20fcb5fdc78bff28b4db2f8d0f0b329101719c0948b3` | same |
| `tokens.txt` | 93939 | `d58544679ea4bc6ac563d1f545eb7d474bd6cfa467f0a6e2c1dc1c7d37e3c35d` | same |
| `Hy-MT2-1.8B-Q4_K_M.gguf` | 1133080448 | `dc5f44fcf1fa496ee7ad725982c0c8c553a4de00259b53af84c4b89fb0c06699` | [tencent/Hy-MT2-1.8B-GGUF @ a0c709d](https://huggingface.co/tencent/Hy-MT2-1.8B-GGUF/tree/a0c709d9fac510f2c807aa3af52872340dc37a4a) |
| `openvoice_v2_tone_color_converter.onnx` | 128448215 | `62523bf068fb6f810b1b66a828c0d5be2f682a023765dc603bf6fefa1d55faca` | [aoiandroid/OpenVoiceV2-ONNX-mirror @ 797733c](https://huggingface.co/aoiandroid/OpenVoiceV2-ONNX-mirror/tree/797733c7bf090d68d8e0d59634e23b032e3f2483), `fp32/tone_color_converter.onnx`, an ONNX export of [myshell-ai/OpenVoiceV2](https://huggingface.co/myshell-ai/OpenVoiceV2) |

## Licences

Each model keeps its makers' licence; the texts are in [`licenses/`](licenses) and attached
to each release.

- **Whisper** — © 2022 OpenAI, MIT ([licenses/whisper-MIT.txt](licenses/whisper-MIT.txt)).
- **Parakeet TDT 0.6B v3** — © NVIDIA, CC-BY-4.0; ONNX int8 export by k2-fsa sherpa-onnx
  (Apache-2.0). Attribution and changes: [licenses/parakeet-CC-BY-4.0-NOTICE.txt](licenses/parakeet-CC-BY-4.0-NOTICE.txt).
- **Hy-MT2 1.8B** — © 2026 Tencent, Apache-2.0 ([licenses/hy-mt2-Apache-2.0.txt](licenses/hy-mt2-Apache-2.0.txt)).
- **OpenVoice V2** — © 2024 MyShell.ai, MIT ([licenses/openvoice-MIT.txt](licenses/openvoice-MIT.txt)).

This repository adds nothing of its own to the models; see each upstream page for how they
were trained and what they are for.
