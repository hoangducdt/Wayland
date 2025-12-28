# Wayland Dotfiles - CachyOS Optimized Configuration

<div align="center">

[🇬🇧 **English**](./README.md) | [🇻🇳 **Tiếng Việt**](./README_VI.md)

</div>

<div align="center">

![Wayland](https://img.shields.io/badge/Wayland-Compositor-blueviolet?style=for-the-badge&logo=wayland)
![CachyOS](https://img.shields.io/badge/CachyOS-Optimized-orange?style=for-the-badge&logo=linux)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
![Maintenance](https://img.shields.io/badge/Maintained-Yes-brightgreen?style=for-the-badge)

**Production-Ready Wayland Desktop Environment for CachyOS**

*Choose between Niri + DankMaterialShell or Hyprland + Caelestia*

[Features](#-features) • [Installation](#-quick-installation) • [Post-Install](#-post-installation-steps) • [Optimizations](#-system-optimizations)

---

</div>

## 🎯 Overview

A complete, **production-tested** Wayland desktop configuration specifically engineered for **CachyOS**, optimized for **AMD Ryzen 7 5800X** and **NVIDIA RTX 3060 12GB**. This is a comprehensive system setup that goes far beyond basic dotfiles.

### 🎨 Choose Your Experience

| **Niri + DankMaterialShell** | **Hyprland + Caelestia** |
|------------------------------|--------------------------|
| 📜 Scrollable-tiling compositor | 🎭 Dynamic tiling compositor |
| 🔄 Smooth horizontal scrolling | ✨ Eye-candy animations |
| 🎯 Productivity-focused workflow | 🎨 Highly customizable experience |
| 🚀 Ultra-responsive performance | 💫 Modern visual effects |

---

## ✨ Features

### 🎨 **Desktop Environment**
- ✅ Two modern Wayland compositor options (Niri/Hyprland)
- ✅ Beautiful, functional shell interfaces (DMS/Caelestia)
- ✅ Complete GTK/Qt theming with multiple icon packs
- ✅ Custom wallpaper collection
- ✅ Professional notification system (Mako for Niri)

### 🚀 **Performance Optimizations**
- ⚡ AMD Ryzen 7 5800X specific CPU tuning
- ⚡ NVIDIA RTX 3060 GPU optimization (without driver changes)
- ⚡ Kernel parameter tuning for Zen 3 architecture
- ⚡ I/O scheduler optimization (BFQ/none)
- ⚡ Network stack optimization (BBR, CAKE)

### 🎮 **Gaming Stack**
- 🎮 Complete gaming setup (Steam, Lutris, Heroic)
- 🎮 Proton-GE and Wine-Staging configured
- 🎮 GameMode CPU governor optimization
- 🎮 MangoHud performance overlay
- 🎮 Xbox controller support (xpadneo)

### 🤖 **AI/ML Development**
- 🧠 CUDA 12.x with cuDNN support
- 🧠 PyTorch with CUDA acceleration
- 🧠 Ollama for local LLM inference
- 🧠 Custom model storage configuration
- 🧠 Docker with NVIDIA Container Toolkit

### 💻 **Development Environment**
- 🛠️ .NET 8.0 & 9.0 SDK
- 🛠️ Unreal Engine 5 dependencies
- 🛠️ Docker & Docker Compose
- 🛠️ Multiple IDEs (Rider, VSCodium)
- 🛠️ Complete build toolchain (Clang, GCC, LLD)

### 🎨 **Creative Suite**
- 🎬 Video editing (Kdenlive, DaVinci Resolve)
- 🖼️ Image editing (GIMP, Krita, Inkscape)
- 🎵 Audio production (Audacity, Ardour)
- 🎥 Streaming setup (OBS Studio with VA-API)
- 🧊 3D creation (Blender with GPU rendering)

### 🌐 **System Features**
- 📡 Vietnamese input method (Fcitx5 + Bamboo)
- 🔒 DNS-over-TLS (Cloudflare + Quad9)
- 🌐 Static IP configuration
- 🔐 Automatic backup system
- 📊 Comprehensive system monitoring

---

## 💻 System Requirements

### Minimum Requirements
- **OS**: CachyOS (latest)
- **CPU**: AMD Ryzen 5000+ series or Intel 10th gen+
- **GPU**: NVIDIA GTX 1000+ series or AMD RX 5000+
- **RAM**: 16GB DDR4
- **Storage**: 50GB free space (100GB+ recommended for AI/ML)

### Optimized For
- **Motherboard**: ROG STRIX B550-XE GAMING WIFI
- **CPU**: AMD Ryzen 7 5800X (8C/16T)
- **GPU**: NVIDIA RTX 3060 12GB
- **RAM**: 32GB+ DDR4

---

## 🚀 Quick Installation

### One-Line Install

```bash
curl -fsSL https://raw.githubusercontent.com/hoangducdt/Wayland/main/install.sh | bash
```

### What Happens During Installation?

1. **Pre-flight Checks**: Validates sudo access and system requirements
2. **Compositor Selection**: Interactive menu to choose Niri or Hyprland
3. **System Update**: Updates CachyOS packages and keyrings
4. **Package Installation**: Installs 200+ carefully selected packages
5. **Configuration**: Symlinks all configuration files
6. **Optimization**: Applies hardware-specific tweaks
7. **Services Setup**: Enables and configures systemd services
8. **Backup Creation**: Backs up existing configurations

**Total Installation Time**: ~30-60 minutes (depending on internet speed)

---

## 📋 Post-Installation Steps

### 1. **Reboot Your System**
```bash
sudo reboot
```
**Why?** Apply kernel modules, NVIDIA settings, and system services.

### 2. **Select Your Compositor at Login**
- Choose **Niri** or **Hyprland** from GDM session menu
- Your choice is saved for future logins

### 3. **Configure Fcitx5 (Vietnamese Input)**
```bash
# Open Fcitx5 Configuration
fcitx5-configtool
```
- Add "Bamboo" input method
- Set toggle key (default: Ctrl+Space)

### 4. **Verify NVIDIA Driver**
```bash
nvidia-smi
```
Expected output: GPU info, driver version, CUDA version

### 5. **Start Ollama for AI/ML** (Optional)
```bash
sudo systemctl start ollama
ollama run llama3.2
```

### 6. **Configure Static IP** (If needed)
Edit `/etc/NetworkManager/system-connections/static-ethernet.nmconnection`
```ini
[ipv4]
method=manual
address1=YOUR_IP/24,YOUR_GATEWAY
dns=1.1.1.1;1.0.0.1;
```

### 7. **Install Additional Fonts** (Optional)
```bash
yay -S ttf-ms-fonts noto-fonts-cjk
```

### 8. **Customize Themes**
- **GTK**: Use `nwg-look` 
- **Qt5/Qt6**: Use `qt5ct` and `qt6ct`
- **Icons**: Multiple packs pre-installed (Papirus, Tela, WhiteSur)

---

## 📦 What's Included

<details>
<summary><b>🖥️ Core System (Click to expand)</b></summary>

- **Display Server**: Wayland with XWayland support
- **Login Manager**: GDM with custom theming
- **File Manager**: Thunar with archive support
- **Terminal**: Kitty (GPU-accelerated)
- **Shell**: Fish with Starship prompt
- **Network**: NetworkManager + iwd
- **Bluetooth**: Bluez + Blueman

</details>

<details>
<summary><b>🎨 Desktop Components</b></summary>

**For Niri:**
- Niri compositor
- DankMaterialShell (DMS)
- Mako notifications
- Swaybg, Swaylock, Swayidle

**For Hyprland:**
- Hyprland compositor
- Caelestia shell (QuickShell-based)
- UWSM session manager
- Hyprland-specific XDG portal

**Common:**
- Fuzzel launcher
- Cliphist clipboard manager
- Hyprpicker color picker
- Brightnessctl brightness control
- Multiple wallpaper collections

</details>

<details>
<summary><b>🎮 Gaming & Entertainment</b></summary>

- **Platforms**: Steam, Lutris, Heroic Games Launcher
- **Compatibility**: Wine-Staging, Proton-GE, DXVK
- **Tools**: MangoHud, GameMode, Gamescope
- **Controllers**: xpadneo (Xbox), general HID support
- **Emulation**: Ready for emulator installation

</details>

<details>
<summary><b>💻 Development Tools</b></summary>

- **Editors**: Neovim, VSCodium, Kate
- **IDEs**: JetBrains Rider
- **Languages**: .NET 8/9, Node.js, Rust, Go, Python 3.x
- **Version Control**: Git, Git LFS, GitHub CLI/Desktop
- **Containers**: Docker, Docker Compose
- **Databases**: PostgreSQL, Redis
- **Build Tools**: CMake, Ninja, Meson, ccache

</details>

<details>
<summary><b>🤖 AI/ML Stack</b></summary>

- **Frameworks**: PyTorch (CUDA), TensorFlow
- **CUDA**: CUDA Toolkit 12.x, cuDNN
- **Inference**: Ollama with custom model storage
- **Libraries**: NumPy, Pandas, Scikit-learn, Transformers
- **Tools**: Jupyter Notebook, LM Studio
- **Docker**: NVIDIA Container Toolkit

</details>

<details>
<summary><b>🎨 Creative Applications</b></summary>

- **3D**: Blender (GPU rendering), Natron
- **Video**: Kdenlive, DaVinci Resolve, OBS Studio
- **Image**: GIMP, Krita, Darktable, RawTherapee
- **Vector**: Inkscape
- **Audio**: Audacity, Ardour, EasyEffects
- **Publishing**: Scribus

</details>

<details>
<summary><b>📊 System Monitoring</b></summary>

- **CPU**: htop, btop, zenmonitor (AMD)
- **GPU**: nvtop, CoreCtrl
- **Network**: iftop, NetworkManager
- **Disk**: GNOME Disks
- **System**: fastfetch, lm_sensors

</details>

---

## ⚡ System Optimizations

### 🔧 CPU Optimizations (Ryzen 7 5800X)

```bash
# CPU Governor
- Performance mode for desktop usage
- Auto-configured via systemd service

# Kernel Parameters
vm.swappiness=10                    # Minimize swap usage
vm.vfs_cache_pressure=50            # Balanced cache pressure
vm.dirty_ratio=10                   # Optimize write buffering
net.core.default_qdisc=cake         # Better network QoS
net.ipv4.tcp_congestion_control=bbr # Modern TCP algorithm
```

### 🎮 GPU Optimizations (RTX 3060)

```bash
# NVIDIA Modprobe Configuration
options nvidia_drm modeset=1 fbdev=1
options nvidia NVreg_PreserveVideoMemoryAllocations=1
options nvidia NVreg_UsePageAttributeTable=1
options nvidia NVreg_DynamicPowerManagement=0x02

# Early Boot Modules
MODULES=(nvidia nvidia_modeset nvidia_uvm nvidia_drm)

# Video Acceleration
- VA-API via nvidia-vaapi-driver
- Hardware video decode/encode
```

### 💾 Storage Optimizations

```bash
# I/O Scheduler
- BFQ for rotating drives (HDD)
- none for NVMe SSDs (optimal)

# File System
- Btrfs support included
- NTFS read/write via ntfs-3g
- exFAT support for external drives
```

### 🌐 Network Optimizations

```bash
# DNS
- Primary: Cloudflare (1.1.1.1, 1.0.0.1)
- Fallback: Quad9, Google DNS
- DNS-over-TLS enabled

# TCP Stack
- BBR congestion control
- CAKE queue discipline
```

### 🎵 Audio Optimizations

```bash
# PipeWire Configuration
- Low-latency audio
- JACK audio server replacement
- EasyEffects for audio processing
- Noise suppression for voice
```

---

## 🎨 Compositor Comparison

| Feature | Niri + DMS | Hyprland + Caelestia |
|---------|------------|----------------------|
| **Tiling Style** | Horizontal scrollable | Dynamic (i3-like) |
| **Animations** | Smooth, minimal | Abundant, customizable |
| **CPU Usage** | Lower | Slightly higher |
| **GPU Usage** | Moderate | Higher (effects) |
| **Customization** | Moderate | Extensive |
| **Learning Curve** | Gentle | Moderate |
| **Stability** | Very stable | Stable |
| **Best For** | Productivity, coding | Visual experience, streaming |

---

## 🔧 Configuration Files Structure

```
~/.config/
├── niri/                      # Niri configuration
│   └── config.kdl
├── DankMaterialShell/         # DMS shell config
├── hypr/                      # Hyprland configuration
│   ├── hyprland/
│   ├── scheme/
│   └── scripts/
├── caelestia/                 # Caelestia shell config
├── kitty/                     # Terminal config
├── fish/                      # Shell config
├── btop/                      # System monitor theme
├── fastfetch/                 # System info config
├── fcitx5/                    # Input method
├── mako/                      # Notifications (Niri)
├── MangoHud/                  # Gaming overlay
├── VSCodium/                  # Editor settings
└── gtk-3.0/                   # GTK theme

~/.local/share/Wayland/        # Installation files
├── Configs/                   # All config files
└── install.sh                 # Installation script
```

---

## 🛠️ Customization Guide

### Change Wallpaper

**Niri:**
```bash
# Edit ~/.config/niri/config.kdl
outputs {
    "DP-1" {
        background-path "/path/to/wallpaper.jpg"
    }
}
```

**Hyprland:**
```bash
# Edit ~/.config/hypr/hyprland/hyprland.conf
exec-once = swaybg -i /path/to/wallpaper.jpg
```

### Customize Keybindings

**Niri:** Edit `~/.config/niri/config.kdl` under `binds` section

**Hyprland:** Edit `~/.config/hypr/hyprland/keybindings.conf`

### Change Shell Theme

**DMS:** Configuration in `~/.config/DankMaterialShell/`

**Caelestia:** 
```bash
caelestia-cli theme list
caelestia-cli theme set <theme-name>
```

### Modify System Monitoring

```bash
# Edit btop config
micro ~/.config/btop/btop.conf

# Edit fastfetch config
micro ~/.config/fastfetch/config.jsonc
```

---

## 📚 Useful Commands

### System Management

```bash
# Update system
sudo pacman -Syu

# Clean package cache
sudo paccache -r

# Check system logs
journalctl -xb

# Monitor system resources
btop
```

### Compositor Control

**Niri:**
```bash
# Reload configuration
niri msg reload-config

# Exit compositor
niri msg exit
```

**Hyprland:**
```bash
# Reload configuration
hyprctl reload

# Get active window info
hyprctl activewindow

# List workspaces
hyprctl workspaces
```

### Docker

```bash
# Start Docker service
sudo systemctl start docker

# Run with GPU support
docker run --gpus all nvidia/cuda:12.0-base nvidia-smi

# Docker Compose
docker-compose up -d
```

### AI/ML (Ollama)

```bash
# Start Ollama service
sudo systemctl start ollama

# Run a model
ollama run llama3.2

# List installed models
ollama list

# Pull new model
ollama pull codellama
```

### Gaming

```bash
# Launch game with MangoHud
mangohud %command%

# Launch with GameMode
gamemoderun %command%

# Check Proton versions
ls ~/.steam/steam/compatibilitytools.d/
```

---

## 🐛 Troubleshooting

### NVIDIA Driver Issues

**Problem:** Black screen after installation

**Solution:**
```bash
# Boot into TTY (Ctrl+Alt+F2)
sudo systemctl disable gdm
sudo mkinitcpio -P
sudo systemctl enable gdm
sudo reboot
```

### Docker Permission Denied

**Problem:** `permission denied while trying to connect to the Docker daemon`

**Solution:**
```bash
# Log out and log back in
# Or manually activate group
newgrp docker
```

### Ollama Model Storage

**Problem:** Models not found or storage issues

**Solution:**
```bash
# Check model directory
ls ~/AI-Models/ollama/

# Verify Ollama service
sudo systemctl status ollama

# Check environment variable
sudo systemctl cat ollama | grep OLLAMA_MODELS
```

### Compositor Won't Start

**Problem:** Compositor crashes on startup

**Solution:**
```bash
# Check logs
journalctl --user -u niri -b
# or
journalctl --user -u hyprland -b

# Verify Wayland session
echo $XDG_SESSION_TYPE
```

### Vietnamese Input Not Working

**Problem:** Fcitx5 Bamboo not responding

**Solution:**
```bash
# Restart Fcitx5
killall fcitx5
fcitx5 -d

# Check environment variables in shell config
echo $GTK_IM_MODULE
echo $QT_IM_MODULE
echo $XMODIFIERS
```

### Audio Issues

**Problem:** No sound or crackling audio

**Solution:**
```bash
# Restart PipeWire
systemctl --user restart pipewire pipewire-pulse wireplumber

# Check audio devices
pactl list sinks

# Verify audio routing
helvum
```

---

## 📊 Performance Benchmarks

### System Boot Time
- **Target**: < 15 seconds to login
- **Compositor Start**: < 3 seconds

### Resource Usage (Idle)

| Compositor | RAM | CPU | GPU VRAM |
|------------|-----|-----|----------|
| Niri + DMS | ~1.2GB | 2-3% | ~400MB |
| Hyprland + Caelestia | ~1.5GB | 3-5% | ~600MB |

### Gaming Performance
- **GameMode**: +5-15% FPS boost
- **MangoHud**: < 1% performance impact
- **Proton Compatibility**: 95%+ Steam library

---

## 🔐 Security Features

- ✅ DNS-over-TLS encryption
- ✅ Automatic system backups
- ✅ GNOME Keyring for password management
- ✅ Polkit authentication agent
- ✅ Firewall ready (configure as needed)
- ✅ Secure boot compatible (NVIDIA modules signed)

---

## 📝 Logging & Backup

### Installation Logs
```bash
~/setup_complete_YYYYMMDD_HHMMSS.log    # Main installation log
~/setup_errors_YYYYMMDD_HHMMSS.log      # Error log
~/install-summary.txt                    # Installation summary
```

### Configuration Backup
```bash
~/Documents/wayland-configs-YYYYMMDD_HHMMSS/  # Backed up configs
```

### State Management
```bash
~/.cache/wayland-setup/setup_state.json  # Installation state tracking
```

---

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<div align="center">

**Made with ❤️ for ROG STRIX B550-XE | Ryzen 7 5800X | RTX 3060 12GB**

**Ready to game, develop, create, and render! 🚀🎮💻🎨**

[⬆ Back to Top](#wayland-dotfiles---cachyos-optimized-configuration)

</div>