# 4× — The Team build

<div align="center"><a href="../README.md">← All builds</a></div>

<img width="1637" height="646" alt="The 4× build — 5U chassis with 4× RTX PRO 6000 Blackwell" src="https://github.com/user-attachments/assets/472e8c4e-d263-4722-87ee-be61cf65fffb" />

Four RTX PRO 6000 Blackwell GPUs on an AMD EPYC platform in an off-the-shelf 5U chassis — no CNC work required. The workstation-class middle option: 384 GB of VRAM for fine-tuning and serving large models to a whole team.

| GPUs | VRAM | Platform | Memory | Power |
|:---|:---|:---|:---|:---|
| 4× NVIDIA RTX PRO 6000 Blackwell | 384 GB | AMD EPYC 9124 on ASRock Rack TURIN2D24G-2L+ | 8× 48 GB DDR5 ECC RDIMM (384 GB) | 3× 2000 W CRPS |

## Build it

1. **Parts** — the [bill of materials](bom/bom.md).
2. **Housing** — the 5U chassis kit ships complete (case, cable harness, power board); the [housing checklist](docs/prepare-me.md) covers unboxing and staging.
3. **Lay out the electronics** — the [component checklist](docs/prepare-ee.md).
4. **Assemble** — the [step-by-step assembly guide](docs/assembly.md).
5. **BIOS, drivers, testing** — the shared [BIOS tuning and GPU testing](../setup.md) guide. Board-specific notes below.

## BIOS notes for this board

The TURIN2D24G-2L+ feeds the GPUs over MCIO, so link width is the setting that matters most (the general list is in [the setup guide](../setup.md)):

```
Advanced -> Chipset Configuration -> PCIE link width
  -> set the MCIO pairs feeding the 4 GPUs to Gen5 x16
Advanced -> PCI Subsystems Settings -> Enable Re-size BAR support
```

Above 4G Decoding is typically enabled by default on this platform — verify it. For exact menu locations, see ASRock Rack's motherboard and BMC manuals for the TURIN2D24G-2L+.

## Testing

All four cards detected, full VRAM, full PCIe width — the checklist is in [the setup guide](../setup.md#gpu-testing).

## Discussion

Alternative build options brainstormed before settling on this baseline — Turin upgrade path, single-socket variants, and a 3× H100 PCIe alternative — with verification notes: [brainstorm & discussion](docs/discussion.md).

## Other builds

The [2× Home build](../2x/README.md) (2× RTX 5090, start tonight) and the [8× On-prem build](../8x/README.md) (8× RTX 4090/5090) scale the same idea down and up.

## License

Open source under the [MIT License](../LICENSE).
