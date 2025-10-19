This is a transcoding script wihich will run in your server containing media which needs to be transcoded named (linux dir).
---
It willl take the files and send them to your powerful machine like your pc or other server (mine is windows laptop so the directory scheme would be different ) if you are using windows (windows wsl should run).
---
read first newww.txt
---
# 🎬 Automated Video Transcoding System

This project automates the video transcoding process between a **Linux server** and a **Windows PC** vai wsl using **FFmpeg** with **GPU acceleration (CUDA/NVENC)**.  
It transfers media files from the server, processes them on the Windows PC for efficient encoding, and then moves the transcoded files back to the server automatically.

---

## 🧭 Overview

This setup is ideal for home media servers where:
- The **Linux server** stores all raw/unprocessed video files.
- The **Windows PC** has a **powerful GPU** (NVIDIA) for hardware-accelerated transcoding.
- The process runs automatically through a **Bash script** that uses **SSH, Rsync, and FFmpeg**.

---

## ⚙️ Requirements

### On Linux Server
- `bash`
- `ssh` and `rsync` configured for passwordless access to the Windows machine (via OpenSSH or WSL)
- Sufficient storage for incoming/outgoing files

### On Windows PC
- `wsl` should be installed and the tools below should be configured
- `FFmpeg` installed (with NVENC/CUDA support)
- `SSH server` enabled
- forward port of wsl so that server can see your wsl and connect to it not to your windows
- NVIDIA GPU drivers with NVENC support

---
