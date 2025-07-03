# Labrat's Home Lab & Engineering Portfolio

Hello! I'm a self-taught, hands-on technologist with a deep passion for Linux, networking, and machine learning. This repository serves as a living document of my home lab environment, personal projects, and the skills I've developed through practical, real-world problem-solving.

My philosophy is simple: **understand the system from the metal up.** I believe the best way to learn is by building, breaking, and fixing. My lab is not just a collection of hardware; it's a dynamic environment for continuous learning and experimentation.

---

## 🛠️ Core Technical Skills

*   **Operating Systems:** Linux (Advanced proficiency in Debian/Ubuntu, Fedora; working knowledge of Arch-based systems), `systemd` & `systemd-boot` management.
*   **Networking & Security:**
    *   Router/Firewall Platform: **pfSense** (management of routing, firewall rules, DHCP, network segmentation).
    *   Concepts: TCP/IP, LAN/WAN, network security fundamentals.
    *   Interests: Red Team / Blue Team methodologies and tools.
*   **Virtualization & Infrastructure:**
    *   Hypervisor: **Proxmox VE** (Bare-metal installation and management).
    *   Technologies: KVM/QEMU, LXC containers.
    *   Experience: Provisioning and managing high-RAM (30GB+) virtual machines for various server roles.
*   **AI / Machine Learning Operations (MLOps):**
    *   Frameworks: **PyTorch**, Hugging Face Transformers, `trl`, `peft`.
    *   Hardware Acceleration: **NVIDIA CUDA** toolkit debugging and environment configuration.
    *   Core Competency: **Bare-metal finetuning of Large Language Models** (e.g., Phi-3, Gemma-3) using QLoRA for VRAM-constrained (6GB) environments.
*   **Programming & Scripting:** Python (Intermediate/Advanced), Bash Scripting.
*   **Development Tools:** Git, Docker (Beginner), `cmake`, `make`, Linux build toolchains.

---

## 🚀 Featured Projects

### 1. Bare-Metal AI Model Finetuning (NVIDIA/CUDA)

This project showcases my ability to work at the challenging intersection of hardware, drivers, and cutting-edge software to achieve a specific goal.

*   **Objective:** Finetune modern LLMs (e.g., `microsoft/Phi-3-mini-4k-instruct`, `google/gemma-3-1b-pt`) on a consumer-grade laptop with a VRAM-constrained NVIDIA RTX 3050 (6GB).
*   **Key Challenges & Solutions:**
    *   **Problem:** Standard `pip` installations of `bitsandbytes` failed to provide GPU acceleration due to environment mismatches.
    *   **Solution:** Engineered a robust, multi-step solution by **compiling the library from source.** This involved using `cmake` to target the CUDA backend specifically, running `make`, and manually placing the compiled shared object (`.so`) libraries to ensure the Python wrappers could link to them correctly. This demonstrated a deep understanding of the compilation and linking process.
    *   **Problem:** Out-of-the-box training scripts caused memory overflows.
    *   **Solution:** Implemented and configured memory-efficient QLoRA finetuning, leveraging 4-bit quantization, gradient checkpointing, and `packing` via the TRL library.
*   **Outcome:** Successfully trained and merged multiple models on hardware that would typically be considered insufficient for the task, proving a deep, practical understanding of MLOps and resource management.
    *   *(You can link to your finetuning scripts here once you upload them to this GitHub repo!)*

### 2. Home Network & Virtualization Infrastructure (Proxmox/pfSense)

This project demonstrates my skills in systems administration, networking, and infrastructure management.

*   **Hardware:** Deployed a dedicated server (upgraded to 32GB RAM) as a bare-metal hypervisor.
*   **Virtualization Layer:** Installed and configured **Proxmox VE** to host and manage all virtualized services.
*   **Network Core:** Implemented **pfSense** as the primary router and firewall for my entire home network, moving beyond consumer-grade hardware to a professional, highly configurable platform.
*   **Capabilities:** The environment is designed to spin up and tear down large virtual machines for development, testing, and learning new technologies in an isolated, controlled manner.

### 3. Multi-OS "Air-Gapped" Workstation

My primary workstation (System76 Gazelle, i9, 64GB RAM) is configured for maximum flexibility and security.

*   **OS Strategy:** Instead of a traditional dual-boot, I run my primary Linux OSes (Fedora, Debian-based) from **physically separate external M.2 and mSATA drives.**
*   **Benefit:** This provides a true "air-gapped" environment where operating systems are completely isolated from one another, preventing bootloader conflicts and enhancing privacy. The internal NVMe drive is dedicated solely to a Windows 11 installation for gaming, using the integrated Intel Iris Xe graphics.
*   **GPU Allocation:** The powerful NVIDIA RTX 3050 is reserved exclusively for Linux environments for dedicated AI/ML and CUDA-accelerated tasks.

---

I am actively seeking a full-time role where I can apply my practical skills and relentless problem-solving mindset to contribute to a technical team. I thrive on challenges and am passionate about learning how systems work from the inside out.# cool_interests
