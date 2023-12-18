---

# Installation Guide for automatic1111 on WSL2

This guide provides step-by-step instructions for installing the automatic1111 tool on Windows Subsystem for Linux 2 (WSL2).

## Prerequisites

Ensure that you have WSL2 installed and set up on your Windows machine. You can follow the official [Microsoft guide](https://docs.microsoft.com/en-us/windows/wsl/install) for setting up WSL2.

## Installation Steps

1. **Update and Upgrade Packages**

   Begin by updating and upgrading your existing packages:

   ```bash
   sudo apt-get update
   sudo apt-get upgrade -y
   ```

2. **Install Required Software**

   Install the necessary software properties:

   ```bash
   sudo apt install software-properties-common -y
   ```

3. **Add Python Repository**

   Add the Python repository using the following command:

   ```bash
   sudo add-apt-repository ppa:deadsnakes/ppa -y
   ```

4. **Install Python and Other Dependencies**

   Install Python 3.10 and other required dependencies:

   ```bash
   sudo apt install unzip git-lfs python3.10 python3.10-venv python3-pip git python3.10-tk ffmpeg libsm6 libxext6 libgl1 wget libcairo2-dev -y
   ```

5. **Install NVIDIA CUDA Toolkit**

### Additional Step: Installing NVIDIA CUDA Deep Neural Network Library (cuDNN)

```bash
sudo DEBIAN_FRONTEND=noninteractive apt-get -yq install nvidia-cudnn
```

   If you have an NVIDIA GPU, install the CUDA toolkit:

   ```bash
   sudo apt install nvidia-cuda-toolkit -y
   ```

   after this just simply run this command:
   ```bash 
   export LD_LIBRARY_PATH=/usr/lib/wsl/lib:$LD_LIBRARY_PATH
   ```

6. **Download and Install automatic1111**

   Use the following command to download and install automatic1111:

   ```bash
   curl -sLS https://raw.githubusercontent.com/stavsap/generative-ai-wsl2/main/text-gen-webui/install.sh | bash -i
   ```

## Post-Installation

After the installation is complete, you can start using the automatic1111 tool. Refer to the official documentation for more details on how to use it effectively.

## Troubleshooting

If you encounter any issues during the installation, please refer to the [Troubleshooting Guide](#) or open an issue in the [GitHub repository](https://github.com/your-repo/automatic1111).

---
