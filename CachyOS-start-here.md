# Local LLM Setup Guide: Intel Arc Pro B50 on CachyOS

This guide covers building `llama.cpp` with SYCL support for Intel GPU acceleration and configuring your environment for persistent access.

## 1. Prerequisites
Install build tools, Intel runtime, and oneAPI toolkit:
```bash
sudo pacman -S --needed base-devel git cmake ninja \
  intel-compute-runtime level-zero-loader vulkan-intel clinfo
yay -S intel-oneapi-base-toolkit

# Add user to hardware groups
sudo usermod -aG render,video $USER
# Log out and back in for changes to take effect
