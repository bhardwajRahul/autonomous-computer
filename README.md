# Build your own Personal AI Computer

**The future of AI is local.** Three reasons:

1. **No one can switch you off.** Last month the US government [took Fable 5 offline](https://www.anthropic.com/news/fable-mythos-access) for most of a month and [gated GPT-5.6 behind an approved-partner list](https://techcrunch.com/2026/06/26/openai-limits-gpt-5-6-rollout-after-government-request-says-restrictions-shouldnt-be-the-norm/). Weights on your own disk can't be revoked.
2. **Your edge stays yours.** Every prompt you send a frontier API carries your product, your process, your edge. [Karp said it](https://www.cnbc.com/video/2026/07/01/palantir-ceo-alex-karp-says-something-has-gone-completely-wrong-with-how-ai-is-sold.html): own the means of production.
3. **It's 20–30× cheaper.** The workload that costs [~$105K/month on GPT-5.5 Pro runs for ~$3–5K on open weights](https://www.benzinga.com/markets/tech/26/06/53048494/chamath-palihapitiya-says-companies-are-overspending-on-ai-as-cheaper-models-rapidly-close-the-gap-burning-through-massive-budgets). On your own machine: electricity.

That's why we open-sourced the whole stack:

- **Hardware — this repo.** Build your own Personal AI Computer in three sizes: every part, every bracket, every BIOS setting, every assembly photo.
- **Software — [Grid](https://github.com/autonomous-ai/autonomous-grid).** Pools your machines behind one OpenAI-compatible endpoint and routes each request to the right model.

**Build it once; own it for good.**

https://github.com/user-attachments/assets/3e410e5d-83f4-4aed-a8b4-2426781f3ebd

## Quick start

1. **Pick a build** below by budget and the models you want to run — [2×](2x/README.md) · [4×](4x/README.md) · [8×](8x/README.md).
2. **Source the parts** from that build's Bill of Materials — [2×](2x/bom/bom.md) · [4×](4x/bom/bom.md) · [8×](8x/bom/bom.md).
3. **Make the housing** — print the STL files or CNC the STEP files — [2×](2x/stl-models) · [8×](8x/step_models). (The 4× uses an off-the-shelf 5U chassis.)
4. **Assemble** — follow the photo-by-photo assembly guide — [2×](2x/docs/assembly.md) · [4×](4x/docs/assembly.md) · [8×](8x/docs/assembly.md).
5. **Software** — [BIOS setup](setup.md), [GPU testing](testing.md), and [Grid](https://github.com/autonomous-ai/autonomous-grid).

## Hardware: Pick your build

There's a build for every budget and use case. Each is a complete, self-contained guide: bill of materials, housing files, wiring, BIOS, and assembly photos.

<table>
<tr>
<td align="center" width="33%">
<a href="2x/README.md"><img src="2x/build-2x.jpg" alt="The 2× build" width="280"></a><br><br>
<a href="2x/README.md"><b>2× — Home</b></a>
</td>
<td align="center" width="33%">
<a href="4x/README.md"><img src="4x/build-4x.jpg" alt="The 4× build" width="280"></a><br><br>
<a href="4x/README.md"><b>4× — Team</b></a>
</td>
<td align="center" width="33%">
<a href="8x/README.md"><img src="8x/build-8x.jpg" alt="The 8× build" width="280"></a><br><br>
<a href="8x/README.md"><b>8× — On-prem business</b></a>
</td>
</tr>
</table>

At a glance:

| Build | GPUs | VRAM | Platform | Power | Housing |
|:---|:---|:---|:---|:---|:---|
| [**2× — Home**](2x/README.md) | 2× RTX 5090 | 64 GB | Intel Xeon W5 (ASUS W790 ACE) | 1× 1600 W | 3D-print or CNC it yourself |
| [**4× — Team**](4x/README.md) | 4× RTX PRO 6000 Blackwell | 384 GB | AMD EPYC 9124 (ASRock Rack TURIN2D24G-2L+) | 3× 2000 W | Off-the-shelf 5U chassis |
| [**8× — On-prem business**](8x/README.md) | 8× RTX 4090 / 5090 | 192–256 GB | 2× AMD EPYC 9004 (ASRock Rack GENOA2D24G-2L+) | 4× 2000 W | CNC-milled anodized aluminum |

## Software

1. **[Setup](setup.md)** — BIOS tuning for multi-GPU, NVIDIA drivers, and your OS.
2. **[Testing](testing.md)** — confirm every GPU is detected, linked at full PCIe width, and stable under load.
3. **[Run Grid](https://github.com/autonomous-ai/autonomous-grid)** — Grid is our open-source orchestration layer for local AI: it pools the computers you already own — this rig, your Mac, the workstation in the corner — behind **one OpenAI-compatible endpoint** and routes each request to whichever machine is running the right model, on your local network or remotely.

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
