<p align="center">
    <img src="photos/8gpu/preparing/ee/inside-8card.jpg" width="700" style="border-radius: 12px; box-shadow: 0 4px 16px #11F73255;">
</p>

<div align="center">

# Autonomous AI Server — 8× GPU Build Guide

<img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License: MIT">
<img src="https://img.shields.io/github/stars/autonomous-ai/autonomous-computer" alt="GitHub stars">
<img src="https://img.shields.io/badge/Status-In%20Development-blue" alt="Status">
<img src="https://img.shields.io/github/downloads/autonomous-ai/autonomous-computer/total" alt="Downloads">
<img src="https://img.shields.io/github/v/release/autonomous-ai/autonomous-computer" alt="Version">
<img src="https://img.shields.io/github/repo-size/autonomous-ai/autonomous-computer" alt="Repo Size">
<img src="https://img.shields.io/github/issues/autonomous-ai/autonomous-computer" alt="Open Issues">
<img src="https://img.shields.io/github/issues-pr/autonomous-ai/autonomous-computer" alt="Open Pull Requests">

</div>

---

<div align="center">
    <b><i>
        This guide shows you how to build a cutting-edge AI server with 8x GPUs. From hardware selection to software setup, follow each step to create a high-performance platform for deep learning, data science, and GPU-intensive workloads.
    </i></b>
</div>

---

## Table of Contents
- [Introduction](#introduction)
- [Preparation](#preparation)
- [Assembly](#assembly)
- [Setup](#setup)
- [Testing](#testing)
- [Bill of Materials](#bill-of-materials)
- [Other Builds](#other-builds)
- [License](#license)

---

## Introduction

<table>
    <tr>
        <td align="center" width="55%">
            <b><i>
                This tutorial is for anyone aiming to build a high-performance AI server with 8 GPUs. Whether you're a researcher, developer, or enthusiast, you'll learn everything from hardware selection and assembly to system configuration and initial testing. Finish with a robust platform ready for demanding AI workloads.
            </i></b>
        </td>
        <td align="center" width="45%">
            <img src="photos/8gpu/introduction/EdgeAI-8GPU-1.png" width="420" height="370" style="border-radius: 8px;">
        </td>
    </tr>
</table>

---

## Preparation

### 1. [Electronic & Electrical](docs/Prepare_EE.md)

### 2. [Mechanical & Housing](docs/Prepare_ME.md)

---

## Assembly

[See detailed steps](docs/Assembly.md)

---

## Setup

### BIOS Optimization for GPU Performance

> **Tip:** The default BIOS settings may not deliver optimal performance for multi-GPU workloads. Adjust these parameters for best results:

- **PCIe Settings** ![Static Badge](https://img.shields.io/badge/Important-8A2BE2)<br>
    Set all PCIe slots to the highest supported speed (Gen4/Gen5) and configure bifurcation for your GPUs.<br>
    ```
    Advanced -> Chipset Configuration -> PCIE link width -> set MCIO2/1, MCIO4/3, MCIO6/5, MCIO8/7, MCIO12/11, MCIO14/13, MCIO16/15, MCIO18/17 to x16
    ```

- **Above 4G Decoding** ![Static Badge](https://img.shields.io/badge/Important-8A2BE2)<br>
    Enable "Above 4G Decoding" to address large GPU memory.<br>
    ```
    May be enabled by default
    ```

- **Resizable BAR** ![Static Badge](https://img.shields.io/badge/Important-8A2BE2)<br>
    Activate "Resizable BAR" for improved CPU-GPU data transfer.<br>
    ```
    Advanced -> PCI Subsystems Settings -> Enable Re-size BAR support
    ```

- **Power Management**<br>
    Disable unnecessary power-saving features (C-states, ASPM) that may throttle GPU performance.<br>
    `Optional`

- **Memory Configuration**<br>
    Set RAM to rated speed and enable XMP/DOCP profiles for max bandwidth.<br>
    `Optional`

- **Fan and Thermal Controls**<br>
    Adjust fan curves and thermal limits for optimal cooling.<br>
    `Optional`

After saving changes, reboot and monitor GPU performance and stability.

**References:**
- [Motherboard User Manual](docs/UM_motherboard.pdf)
- [BMC Documents](docs/UM_BMC.pdf)

<p align="center">
    <video src="https://github.com/user-attachments/assets/41cd6d5d-9acd-41d6-b9c2-4da4666f3870" controls width="700">
        <a href="https://github.com/user-attachments/assets/41cd6d5d-9acd-41d6-b9c2-4da4666f3870">How-to-set-up-BIOS.mp4</a>
    </video>
</p>

---

## Testing

Boot with WinPE from USB to verify hardware, or install Linux, NVIDIA drivers, and check with `nvtop`. Once confirmed, install your OS and start your AI work.

<table>
    <tr>
        <td align="center">
            <img src="photos/8gpu/testing/Nvtop.png" width="700"><br>
        </td>
        <td align="center">
            <img src="photos/8gpu/assembly/40.png" width="400"><br>
        </td>
    </tr>
</table>

<p align="center">
    <video src="https://github.com/user-attachments/assets/71afbc5c-ae69-410e-868a-a52b915b1e7a" controls width="700">
        <a href="https://github.com/user-attachments/assets/71afbc5c-ae69-410e-868a-a52b915b1e7a">Booting.mp4</a>
    </video>
</p>

---

## Bill of Materials

- [Bill of Materials](bom/BOM.md)

---

## Other Builds

<table>
    <tr>
        <td align="center" width="50%">
            <a href="2x-rtx5090/README.md">
                <img src="2x-rtx5090/photos/2gpu/introduction/introduction.png" width="420" style="border-radius: 8px;">
            </a>
            <br><b>2× RTX 5090</b> — Intel Xeon W5 + ASUS W790<br>
            <a href="2x-rtx5090/README.md">View Build Guide →</a>
        </td>
        <td align="center" width="50%">
            <a href="4x-rtx-pro-6000/README.md">
                <img src="4x-rtx-pro-6000/photos/4gpu/introduction/rack1.jpg" width="420" style="border-radius: 8px;">
            </a>
            <br><b>4× RTX PRO 6000 Blackwell</b> — AMD EPYC 9124 + ASRock Rack<br>
            <a href="4x-rtx-pro-6000/README.md">View Build Guide →</a>
        </td>
    </tr>
</table>

---

## License

This project is open source under the [MIT License](LICENSE).
