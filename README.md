# Build your own Personal AI Computer

https://github.com/user-attachments/assets/36f7aa02-42ac-4b35-b757-a5dd3b43ef1a

**The future of AI is local.** Three reasons:

1. **No one can switch you off.** In June 2026 the US government took Fable 5 offline for most of a month and gated GPT-5.6 behind an approved-partner list. Weights on your own disk can't be revoked.
2. **Your business is their training data.** Every prompt you send OpenAI or Anthropic carries your product, your process, your edge. They will turn your secret sauce into their product.
3. **Inference becomes free.** Open weights on a cloud API already cut the bill 20–30×. On your own machine there is no bill at all. No API, no meter.

We built the whole stack, hardware and software, designed together. Then we open-sourced all of it:

- **Hardware — this repo.** Your Personal AI Computer in three sizes: every part, every bracket, every BIOS setting, every assembly photo.
- **Software — your choice.** Run any local AI framework — vLLM, Ollama, llama.cpp — or [Grid](https://github.com/autonomous-ai/autonomous-grid), our local AI orchestrator.

## Quick start

1. **Pick a build** below by budget and the models you want to run — [2×](2x/README.md) · [4×](4x/README.md) · [8×](8x/README.md).
2. **Source the parts** from that build's Bill of Materials — [2×](2x/bom/bom.md) · [4×](4x/bom/bom.md) · [8×](8x/bom/bom.md).
3. **Make the housing** — print the STL files or CNC the STEP files — [2×](2x/stl-models) · 4× · [8×](8x/step_models).
4. **Assemble** — follow the photo-by-photo assembly guide — [2×](2x/docs/assembly.md) · [4×](4x/docs/assembly.md) · [8×](8x/docs/assembly.md).
5. **BIOS tuning and GPU testing** — [one guide](setup.md): the settings that matter, then prove every card runs at full width.
6. **Serve your models** — any local AI framework, or [Grid](https://github.com/autonomous-ai/autonomous-grid), our local AI orchestrator.

## Hardware: Pick your build

There's a build for every budget and use case. Each is a complete, self-contained guide: bill of materials, housing files, wiring, BIOS, and assembly photos.

### 2× — Home

2× RTX 5090. Enough for Llama, Qwen, and DeepSeek with quantization. Run OpenClaw, Hermes Agent, or your own LangChain stack locally.

**64 GB VRAM · 192 GB RAM · 1600 W · print or CNC the housing yourself**

<a href="2x/README.md"><img src="2x/photos/gallery/hero.webp" alt="The 2× build — two RTX 5090s on the open frame"></a>

<table>
<tr>
<td width="50%"><img src="2x/photos/gallery/riser-frame.webp" alt="Mounting the PCIe 5.0 risers"></td>
<td width="50%"><img src="2x/photos/gallery/fan-tray.webp" alt="The fan tray"></td>
</tr>
<tr>
<td width="50%"><img src="2x/photos/gallery/side-panel.webp" alt="Closing the side panel"></td>
<td width="50%"><img src="2x/photos/gallery/finished.webp" alt="The finished 2× on a desk"></td>
</tr>
</table>

**[Build the 2× →](2x/README.md)**

### 4× — Team

4× RTX PRO 6000 Blackwell in a 5U chassis. Built for the larger open models — Kimi, MiniMax, GLM. No API bills. Low latency. Private data.

**384 GB VRAM · 384 GB RAM · 3× 2000 W · off-the-shelf 5U chassis, no CNC work**

<a href="4x/README.md"><img src="4x/build-4x.jpg" alt="The 4× build — four RTX PRO 6000 Blackwell in the 5U chassis"></a>

**[Build the 4× →](4x/README.md)**

### 8× — On-prem business

8× RTX 4090 or 5090 on dual EPYC. A local inference box for teams shipping with open models. Develop, serve, fine-tune — the work that should never leave your floor.

**192–256 GB VRAM · 8000 W · CNC-milled, anodized aluminum housing**

<a href="8x/README.md"><img src="8x/photos/gallery/hero.webp" alt="The 8× build — eight GPUs in the anodized aluminum housing"></a>

<table>
<tr>
<td width="50%"><img src="8x/photos/gallery/parts-layout.webp" alt="Every part laid out before assembly"></td>
<td width="50%"><img src="8x/photos/gallery/cnc-milling.webp" alt="CNC-milling the housing"></td>
</tr>
<tr>
<td width="50%"><img src="8x/photos/gallery/gpu-install.webp" alt="Installing the GPUs"></td>
<td width="50%"><img src="8x/photos/gallery/finished.webp" alt="The finished 8× on a desk"></td>
</tr>
</table>

**[Build the 8× →](8x/README.md)**

## Software

1. **[BIOS tuning and GPU testing](setup.md)** — multi-GPU BIOS settings, NVIDIA drivers, and confirming every GPU is detected, linked at full PCIe width, and stable under load.
2. **[Run Grid](https://github.com/autonomous-ai/autonomous-grid)** — Grid is our open-source orchestration layer for local AI: it pools the computers you already own — this rig, your Mac, the workstation in the corner — behind **one OpenAI-compatible endpoint** and routes each request to whichever machine is running the right model, on your local network or remotely.

   ```bash
   curl -fsSL https://grid.autonomous.ai/install.sh | bash
   ```

## Contributing

Built one? Improved a part? Found a better component? See [**CONTRIBUTING.md**](CONTRIBUTING.md) — and [share your build](https://github.com/autonomous-ai/autonomous-computer/issues/new?template=share-your-build.md). The best community builds get featured.

## License

Open source under the [MIT License](LICENSE). Fork it, change it, build your own and sell it — we just want it built.

---

<div align="center">
<b>Autonomous</b> — the AI hardware company.<br>
Questions? <a href="https://github.com/autonomous-ai/autonomous-computer/issues">Open an issue.</a>
</div>
