<p align="center">
    <a href="https://git.io/typing-svg">
        <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=32&duration=1800&pause=600&color=11F732&background=000000&width=1000&height=110&lines=Welcome+-+where+8%C3%974090Ds+become+your+new+roommate." alt="Typing SVG" />
    </a>
</p>

<p align="center">
    <img src="Photos/8GPU/Preparing/EE/inside-8card.jpg" width="700" style="border-radius: 12px; box-shadow: 0 4px 16px #11F73255;">
</p>

<div align="center">

<img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License: MIT">
<img src="https://img.shields.io/github/stars/AutonomousOfficial/8xGPUs" alt="GitHub stars">
<img src="https://img.shields.io/badge/Status-In%20Development-blue" alt="Status">
<img src="https://img.shields.io/github/downloads/AutonomousOfficial/8xGPUs/total" alt="Downloads">
<img src="https://img.shields.io/github/v/release/AutonomousOfficial/8xGPUs" alt="Version">
<img src="https://img.shields.io/github/repo-size/AutonomousOfficial/8xGPUs" alt="Repo Size">
<img src="https://img.shields.io/github/issues/AutonomousOfficial/8xGPUs" alt="Open Issues">
<img src="https://img.shields.io/github/issues-pr/AutonomousOfficial/8xGPUs" alt="Open Pull Requests">

</div>

---

<div align="center">
    <b><i>
        This guide shows you how to build a cutting-edge AI server with 8x GPUs. From hardware selection to software setup, follow each step to create a high-performance platform for deep learning, data science, and GPU-intensive workloads.
    </i></b>
</div>

---

## 📚 Table of Contents
- [Introduction](#-🏁-introduction)
- [Preparation](#-🛠️-preparation)
- [Assembly](#-🤖-assembly)
- [Setup](#-⚙️-setup)
- [Testing](#-🧪-testing)
- [BOM](#-📦-bill-of-materials-bom)
- [License](#-📝-license)

---

# 🏁 Introduction &ensp; [🔝](#-table-of-contents)

<table>
    <tr>
        <td align="center" width="55%">
            <b><i>
                This tutorial is for anyone aiming to build a high-performance AI server with 8 GPUs. Whether you're a researcher, developer, or enthusiast, you'll learn everything from hardware selection and assembly to system configuration and initial testing. Finish with a robust platform ready for demanding AI workloads.
            </i></b>
        </td>
        <td align="center" width="45%">
            <img src="Photos/8GPU/Introduction/EdgeAI-8GPU-1.png" width="420" height="370" style="border-radius: 8px;">
        </td>
    </tr>
</table>

---

# 🛠️ Preparation &ensp; [🔝](#-table-of-contents)

### 1. [**Electronic & Electrical**](https://github.com/AutonomousOfficial/8xGPUs/blob/main/Docs/Prepare_EE.md)

### 2. [**Mechanical & Housing**](https://github.com/AutonomousOfficial/8xGPUs/blob/main/Docs/Prepare_ME.md)

---

# 🤖 Assembly &ensp; [🔝](#-table-of-contents)
[See detailed steps](https://github.com/AutonomousOfficial/8xGPUs/blob/main/Docs/Assembly.md)

---

# ⚙️ Setup &ensp; [🔝](#-table-of-contents)
### BIOS Optimization for GPU Performance

> **Tip:** The default BIOS settings may not deliver optimal performance for multi-GPU workloads. Adjust these parameters for best results:

- **PCIe Settings** ![Static Badge](https://img.shields.io/badge/Important-8A2BE2)<br>
    🚨📢🔔⚠️
    Set all PCIe slots to the highest supported speed (Gen4/Gen5) and configure bifurcation for your GPUs.<br>
    ```
    Advanced -> Chipset Configuration -> PCIE link width -> set MCIO2/1, MCIO4/3, MCIO6/5, MCIO8/7, MCIO12/11, MCIO14/13, MCIO16/15, MCIO18/17 to x16
    ```

- **Above 4G Decoding** ![Static Badge](https://img.shields.io/badge/Important-8A2BE2)<br>
    🚨📢🔔⚠️
    Enable "Above 4G Decoding" to address large GPU memory.<br>
    ```
    May be enabled by default
    ```

- **Resizable BAR** ![Static Badge](https://img.shields.io/badge/Important-8A2BE2)<br>
    🚨📢🔔⚠️
    Activate "Resizable BAR" for improved CPU-GPU data transfer.<br>
    ```
    Advanced -> PCI Subsystems Settings -> Enable Re-size BAR support
    ```

- **Power Management**  
    Disable unnecessary power-saving features (C-states, ASPM) that may throttle GPU performance.<br>
    `Optional`

- **Memory Configuration**  
    Set RAM to rated speed and enable XMP/DOCP profiles for max bandwidth.<br>
    `Optional`

- **Fan and Thermal Controls**  
    Adjust fan curves and thermal limits for optimal cooling.<br>
    `Optional`

After saving changes, reboot and monitor GPU performance and stability.

**References:**  
- [Motherboard User Manual 💻🖱️](https://download.asrock.com/Manual/GENOA2D24G-2L%2b.pdf)  
- [BMC Documents 🤖](https://download.asrock.com/Manual/BMC/GENOA2D24G-2L%2b.pdf)

<p align="center">
    <video src="https://github.com/user-attachments/assets/41cd6d5d-9acd-41d6-b9c2-4da4666f3870"></video>
</p>

---

# 🧪 Testing &ensp; [🔝](#-table-of-contents)

Boot with WinPE from USB to verify hardware, or install Linux, NVIDIA drivers, and check with `nvtop`. Once confirmed, install your OS and start your AI work.

<table>
    <tr>
        <td align="center">
            <img src="Photos/8GPU/Testing/Nvtop.png" width="700"><br>
        </td>
        <td align="center">
            <img src="Photos/8GPU/Assembly/40.png" width="400"><br>
        </td>
    </tr>
</table>

<p align="center">
    <video src="https://github.com/user-attachments/assets/71afbc5c-ae69-410e-868a-a52b915b1e7a"></video>
</p>

---

# 📦 Bill of Materials (BOM) &ensp; [🔝](#-table-of-contents)

- [𝄜 Bill of Materials](https://github.com/AutonomousOfficial/8xGPUs/blob/main/BOM/BOM.md)

---

# 📝 License &ensp; [🔝](#-table-of-contents)

This project is open source under the [MIT License](https://github.com/AutonomousOfficial/8xGPUs/blob/main/LICENSE).

---

<p align="center">
  <a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.demolab.com?font=Fira+Code&duration=1800&pause=1000&color=11F732&width=840&lines=If+this+helped%2C+toss+us+a+%E2%AD%90.+Got+questions%3F+Email+brody%40autonomous.ai" alt="Typing SVG" /></a>
</p>
