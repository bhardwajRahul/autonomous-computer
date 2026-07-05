# 4× NVIDIA RTX 5090

<img src="photos/gallery/hero.webp" alt="The 4× 5090 build — airflow through the dual-chamber housing">

The team build: four RTX 5090s in a dual-chamber desktop cube — fans and PSUs breathe below, GPUs live above. Built for larger open models like Kimi, MiniMax, and GLM. No API bills. Low latency. Private data.

- **4× NVIDIA RTX 5090** — 128 GB VRAM · 7,168 GB/s · 838 FP32 TFLOPS
- **AMD Ryzen Threadripper Pro** · 96 GB RAM · 1 TB NVMe
- **PCIe Gen 5 ×16** per GPU · 2× 10 GbE · BMC
- **2,750 W draw** · 4,000 W PSU
- **15.5″ × 15.5″ × 16″** · 66 lb

**The full build guide — bill of materials, housing files, photo-by-photo assembly — is in progress.** The photos below are from our build. Want it sooner? [Open an issue](https://github.com/autonomous-ai/autonomous-computer/issues) and tell us.

## The build

<table>
<tr>
<td width="50%"><img src="photos/gallery/fan-chassis.webp" alt="Motherboard on the fan chassis"></td>
<td width="50%"><img src="photos/gallery/psu-cabling.webp" alt="Cabling the power supplies"></td>
</tr>
<tr>
<td width="50%"><img src="photos/gallery/cooler-mount.webp" alt="Mounting a GPU to the frame"></td>
<td width="50%"><img src="photos/gallery/gpu-stack.webp" alt="All four RTX 5090s on the frame"></td>
</tr>
</table>

<img src="photos/gallery/finished.webp" alt="The finished 4× 5090">

## Serve your models

The rig runs, now put it to work. The easiest way is [Grid](https://github.com/autonomous-ai/autonomous-grid), the open orchestrator for local AI: it pools your machines into one local AI network. Or run any local AI engine — vLLM, Ollama, llama.cpp.

```bash
curl -fsSL https://grid.autonomous.ai/install.sh | bash
```

<img width="2200" height="1452" alt="Grid — your machines pooled into one local AI network" src="https://github.com/user-attachments/assets/0ad98393-248a-40bd-9877-e6f0847c7b0e" />

## Other builds

The [2× 5090](../2x-5090/README.md) (start tonight), the [4× 6000](../4x-6000/README.md) (384 GB VRAM), and the [8× 5090](../8x-5090/README.md) (on-prem scale) are complete guides today.

## License

Open source under the [MIT License](../LICENSE).
