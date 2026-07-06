# Assembly

Order of assembly for one 5U server — the TURIN2D24G-2L+ board, one EPYC 9124, and four RTX PRO 6000 GPUs in the ASRock 5U chassis. Step photos are added as the build is documented.

| Step | Description |
|:----:|:------------|
|  1   | Prepare all components — the [electronics checklist](prepare-ee.md) and the [housing prep](prepare-me.md). |
|  2   | Install the CPU into the SP5 socket on the TURIN2D24G-2L+ motherboard. |
|  3   | Mount the COOLSERVER 2U SP5 S22 heatsink onto the CPU. |
|  4   | Populate the 8 DDR5 ECC RDIMMs (48 GB each, 384 GB total), following the board's DIMM population order. |
|  5   | Install the Samsung 990 EVO Plus NVMe SSD into the M.2 slot. |
|  6   | Seat the motherboard in the 5U chassis and secure it with the standoffs and screws. |
|  7   | Install the three CRPS PSUs and connect them to the power board. |
|  8   | Route the motherboard and peripheral power cables from the power board. |
|  9   | Install the four NVIDIA RTX PRO 6000 Blackwell GPUs and secure them to the support rail. |
|  10  | Connect the GPU power cables and verify the retention clips. |
|  11  | Connect the MCIO cables between the motherboard and the GPU PCIe risers. |
|  12  | Connect the chassis fans to the fan board and verify the PWM headers. |
|  13  | Close the chassis, connect the AC inlet, and perform first-boot. |

---
