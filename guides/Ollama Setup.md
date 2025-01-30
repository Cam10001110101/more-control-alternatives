# Installing Ollama: A Step-by-Step Guide

This guide walks through installing Ollama on Windows, macOS, and Docker Desktop.

### Choosing Your Installation Method

* **Native Installation** (Recommended for most users)
  * Available for Linux, macOS, and Windows
  * Easiest to set up and use
  * Best performance for most use cases
  * Integrates naturally with your operating system
  * Ideal for personal use and learning

* **Docker Installation**
  * Better for development and testing
  * Easier to manage multiple versions
  * Useful when working across different environments
  * Recommended if you're already using Docker for other projects
  * Good for isolation and clean uninstallation

## Hardware Requirements

### Basic System Requirements

| Component | Minimum Requirement |
|-----------|-------------------|
| Operating System | Windows 11/10, macOS 12+, or Linux with kernel 5.12+ |
| Storage Type | SSD Recommended |
| Internet | Stable Connection Required |

### Model to Resources Pairing

| Specification | Entry Level<br>(1B-3B) | Mid-Range<br>(3B-7B) | High-End<br>(13B+) |
|--------------|----------------------|-------------------|----------------|
| CPU | 4 cores, 2.5GHz+ | 6+ cores, 3.0GHz+ | 8+ cores, 3.5GHz+ |
| RAM | 8GB | 16GB | 32GB+ |
| GPU | Integrated/4GB VRAM | 8GB+ VRAM<br>(RTX 3060+) | 12GB+ VRAM<br>(RTX 4070+) |
| LLM Disk Use | 1-5GB | 10-25GB+ | 50-300GB+ |

### Recommended Models

| Tier | Models |
|------|---------|
| Entry Level | • tiny-llama<br>• neural-chat<br>• phi<br>• gemma-2b |
| Mid-Range | • mistral<br>• neural-chat<br>• llama2<br>• gemma-7b |
| High-End | • llama2:13b<br>• mixtral<br>• solar<br>• codellama |

### Performance Expectations

| Metric | Entry Level | Mid-Range | High-End |
|--------|-------------|-----------|-----------|
| Response Time | 5-15s | 2-8s | 1-5s |
| Memory Usage | 4-6GB | 8-12GB | 16-24GB+ |

> **Note**: Performance metrics are approximate and may vary based on specific hardware configurations and model optimizations.

## Windows Installation

### Prerequisites
* Windows 10/11

### Steps

1. **Download Ollama**
   * Visit [Ollama's website](https://ollama.com/download)
   * Click the Windows download button

2. **Install the Application**
   * Run the downloaded installer
   * Follow the installation wizard prompts
   * Ollama will start automatically after installation

4. **Verify Installation**
   ```bash
   ollama --version
   ```

## macOS Installation

### Prerequisites
* macOS 12 (Monterey) or newer
* Apple Silicon (M1/M2/M3) or Intel processor

### Steps

1. **Download Ollama**
   * Visit [Ollama's website](https://ollama.com/download)
   * Click the macOS download button

2. **Install the Application**
   * Open the downloaded .dmg file
   * Drag Ollama to your Applications folder
   * Double-click Ollama in Applications to start it

3. **First-time Setup**
   * Click "Open" if you see a security prompt
   * Ollama will appear in your menu bar

4. **Verify Installation**
   ```bash
   ollama --version
   ```

## Linux Installation

### Prerequisites
* Linux x86_64 system
* `curl` installed
* Administrator/sudo access

### Steps

1. **Install Ollama**
   ```bash
   curl -fsSL https://ollama.com/install.sh | sh
   ```

2. **Start Ollama Service**
   ```bash
   systemctl start ollama
   ```
   If using non-systemd Linux:
   ```bash
   ollama serve
   ```

3. **Verify Installation**
   ```bash
   ollama --version
   ```

### Common Linux Distributions

#### Ubuntu/Debian
* Ensure curl is installed:
  ```bash
  sudo apt update && sudo apt install curl
  ```

#### Fedora/RHEL
* Ensure curl is installed:
  ```bash
  sudo dnf install curl
  ```

## Docker Desktop Installation

### Prerequisites
* Docker Desktop installed and running
* Basic familiarity with Docker commands

### Steps

1. **Pull the Ollama Image**
   ```bash
   docker pull ollama/ollama
   ```

2. **Run Ollama Container**
   ```bash
   docker run -d -v ollama:/root/.ollama -p 11434:11434 --name ollama ollama/ollama
   ```

3. **Verify Container**
   ```bash
   docker ps
   ```
   You should see the Ollama container running

## Testing Your Installation

After installing, test your setup:

1. **Pull a Model**
   ```bash
   ollama pull deepseek-r1:1.5b
   ```

2. **Run a Basic Test**
   ```bash
   ollama run deepseek-r1:1.5b "Hello, how are you?"
   ```

## Troubleshooting Common Issues

### Windows
* If the installer doesn't run, ensure Windows is fully updated
* If you see a Windows Defender prompt, click 'More Info' and then 'Run Anyway'
* Performance issues: Verify you have at least 8GB RAM and 10GB free disk space
* If Ollama doesn't start: Check Windows Services app to ensure the Ollama service is running

### macOS
* "App can't be opened" - Right-click the app and select Open
* Performance issues - Ensure you have enough free disk space
* CPU compatibility - Verify you're using the correct version for your processor

### Docker
* Port conflicts - Ensure nothing else is using port 11434
* Container won't start - Check Docker logs: `docker logs ollama`
* Memory issues - Increase Docker's resource limits in settings

## Next Steps

* [Explore available models](https://ollama.com/library)

## Additional Resources

* [Official Ollama Documentation](https://github.com/ollama/ollama/tree/main/docs)
* [Docker Documentation](https://docs.docker.com/)

---

*Last updated: January 30, 2025*