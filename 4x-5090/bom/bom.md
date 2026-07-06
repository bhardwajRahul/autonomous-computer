# Bill of Materials

Quantities are per machine — one 4× RTX 5090 build. Part photos are in the [component checklist](../docs/prepare-ee.md).

> Draft — exact models marked **TBD** are pending confirmation from the build team.

| No  | Item              | Detail                                     | Qty | Category   | Notes                                                              |
|:---:|:------------------|:-------------------------------------------|:---:|:-----------|:------------------------------------------------------------------|
|  1  | Mainboard         | AMD WRX90 workstation board (model **TBD**)|  1  | Mainboard  | sTR5 socket; 2× 10 GbE + BMC per spec                             |
|  2  | CPU               | AMD Ryzen Threadripper PRO (model **TBD**) |  1  | Processor  | sTR5 socket                                                       |
|  3  | CPU heatsink      | sTR5-compatible cooler                     |  1  | Cooling    |                                                                   |
|  4  | RAM               | DDR5 96 GB total                           |  —  | Memory     | DIMM count **TBD** (per board's channel layout)                  |
|  5  | SSD               | 1 TB NVMe                                   |  1  | Storage    | Capacity configurable                                             |
|  6  | GPU               | MSI GeForce RTX 5090                        |  4  | Graphics   | 32 GB each — 128 GB total                                        |
|  7  | PCIe 5.0 riser    | PCIe 5.0 x16 riser cable                   |  4  | Cable      | One per GPU                                                       |
|  8  | PSU               | 4000 W (e.g. 2× 2000 W — **TBD**)          |  1  | Power      | 2,750 W draw                                                     |
|  9  | GPU power cable   | 12V-2x6 / 12VHPWR, 600 W rated             |  4  | Cable      | One per GPU                                                       |
| 10  | Power cord        | Wall cord rated for the PSU                 |  1  | Cable      |                                                                   |
| 11  | Fan               | Case fan                                    |  4  | Cooling    |                                                                   |
| 12  | Frame housing     | Full housing set — **same cube as the 2×** |  1  | Housing    | Print the [STLs](../../2x-5090/stl-models) or CNC the [STEPs](../../2x-5090/step_models) |
