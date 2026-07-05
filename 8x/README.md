# 8× — The On-prem Business build

<div align="center"><a href="../README.md">← All builds</a></div>

https://github.com/user-attachments/assets/36f7aa02-42ac-4b35-b757-a5dd3b43ef1a

The largest build: eight GPUs on a dual-EPYC (Genoa) platform in a CNC-milled, anodized aluminum housing. A team's AI on your own floor, where your IP and data never leave the building.

| GPUs | VRAM | Platform | Memory | Power |
|:---|:---|:---|:---|:---|
| 8× NVIDIA RTX 4090 or 5090 | 192–256 GB | 2× AMD EPYC 9004 (Genoa) on ASRock Rack GENOA2D24G-2L+ | DDR5 ECC (up to 24 DIMMs) | 4× PSU, 8000 W total |

## Build it

1. **Parts** — the [bill of materials](bom/bom.md).
2. **Housing** — CNC the [STEP files](step_models) (STL versions in [stl-models](stl-models)), then sand-blast and anodize — the [housing guide](docs/prepare-me.md) shows the process.
3. **Lay out the electronics** — the [component checklist](docs/prepare-ee.md), with a photo of every part.
4. **Assemble** — the [photo-by-photo assembly guide](docs/assembly.md), 39 steps from bare plates to a running machine.
5. **BIOS, drivers, testing** — the shared [BIOS tuning and GPU testing](../setup.md) guide. Board-specific notes below.

## BIOS notes for this board

The GENOA2D24G-2L+ feeds the GPUs over MCIO, so link width is the setting that matters most (the general list is in [the setup guide](../setup.md)):

```
Advanced -> Chipset Configuration -> PCIE link width
  -> set MCIO2/1, MCIO4/3, MCIO6/5, MCIO8/7, MCIO12/11, MCIO14/13, MCIO16/15, MCIO18/17 to x16
Advanced -> PCI Subsystems Settings -> Enable Re-size BAR support
```

Above 4G Decoding is typically enabled by default on this platform — verify it.

Board references: [motherboard manual](docs/um-motherboard.pdf) · [BMC manual](docs/um-bmc.pdf)

## Testing

All eight cards detected, full VRAM, full PCIe width — the checklist is in [the setup guide](../setup.md#gpu-testing).

<table>
    <tr>
        <td align="center">
            <img src="photos/8gpu/testing/Nvtop.png" width="700">
        </td>
        <td align="center">
            <img src="photos/8gpu/assembly/40.png" width="400">
        </td>
    </tr>
</table>

## Other builds

Smaller footprint? The [2× Home build](../2x/README.md) (2× RTX 5090, start tonight) and the [4× Team build](../4x/README.md) (4× RTX PRO 6000 Blackwell, 384 GB VRAM) use the same playbook.

## License

Open source under the [MIT License](../LICENSE).
