# 2× — The Home build

<div align="center"><a href="../README.md">← All builds</a></div>

<p align="center">
    <img src="photos/2gpu/introduction/introduction.png" width="700">
</p>

Two RTX 5090s on an Intel Xeon W platform, in a housing you print or CNC yourself. This is the build you can start tonight: desk-sized, runs on a normal wall outlet, and big enough for serious local models.

| GPUs | VRAM | Platform | Memory | Power |
|:---|:---|:---|:---|:---|
| 2× NVIDIA RTX 5090 | 64 GB | Intel Xeon W5 on ASUS W790 ACE | 4× DDR5 | 1× 1600 W PSU |

## Build it

1. **Parts** — the [bill of materials](bom/bom.md).
2. **Housing** — print the [STL files](stl-models) or CNC the [STEP files](step_models).
3. **Lay out the electronics** — the [component checklist](docs/prepare-ee.md), with a photo of every part.
4. **Assemble** — the [photo-by-photo assembly guide](docs/assembly.md), 23 steps from bare housing to closed box.
5. **BIOS, drivers, testing** — the shared [BIOS tuning and GPU testing](../setup.md) guide. Board-specific notes below.

## BIOS notes for this board

The two settings that matter on the W790 (the general list is in [the setup guide](../setup.md)):

```
Advanced -> PCI Subsystems Settings -> Enable Above 4G Decoding
Advanced -> PCI Subsystems Settings -> Enable Re-size BAR support
```

Board references: [motherboard manual](docs/um-motherboard.pdf) · [BIOS manual](docs/um-bios.pdf)

## Testing

Both cards detected, full VRAM, full PCIe width — the checklist is in [the setup guide](../setup.md#gpu-testing).

<p align="center">
    <img src="photos/2gpu/testing/nvidia-smi.png" width="700">
</p>

## Other builds

Need more? The [4× Team build](../4x/README.md) (4× RTX PRO 6000 Blackwell, 384 GB VRAM) and the [8× On-prem build](../8x/README.md) (8× RTX 4090/5090) scale the same idea up.

## License

Open source under the [MIT License](../LICENSE).
