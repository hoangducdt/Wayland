# Wayland Dotfiles - Cấu Hình Tối Ưu Cho CachyOS

<div align="center">

[**Tiếng Việt**](README_VI.md) | [**English**](README.md)

</div>

<div align="center">

![Wayland](https://img.shields.io/badge/Wayland-Compositor-blueviolet?style=for-the-badge&logo=wayland)
![CachyOS](https://img.shields.io/badge/CachyOS-Optimized-orange?style=for-the-badge&logo=linux)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
![Maintenance](https://img.shields.io/badge/Maintained-Yes-brightgreen?style=for-the-badge)

**Môi Trường Desktop Wayland Sẵn Sàng Triển Khai Cho CachyOS**

*Lựa chọn giữa Niri + DankMaterialShell hoặc Hyprland + Caelestia*

[Tính năng](#-tính-năng) • [Cài đặt](#-cài-đặt-nhanh) • [Sau cài đặt](#-các-bước-sau-cài-đặt) • [Tối ưu hóa](#-tối-ưu-hóa-hệ-thống)

---

</div>

## 🎯 Tổng Quan

Một cấu hình desktop Wayland hoàn chỉnh, **đã được kiểm nghiệm thực tế**, được thiết kế đặc biệt cho **CachyOS**, tối ưu hóa cho **AMD Ryzen 7 5800X** và **NVIDIA RTX 3060 12GB**. Đây là một thiết lập hệ thống toàn diện vượt xa khái niệm dotfiles cơ bản.

### 🎨 Lựa Chọn Trải Nghiệm Của Bạn

| **Niri + DankMaterialShell** | **Hyprland + Caelestia** |
|------------------------------|--------------------------|
| 📜 Compositor xếp cửa sổ kiểu cuộn | 🎭 Compositor xếp cửa sổ động |
| 🔄 Cuộn ngang mượt mà | ✨ Hiệu ứng hoạt hình bắt mắt |
| 🎯 Luồng làm việc tập trung năng suất | 🎨 Trải nghiệm tùy biến cao |
| 🚀 Hiệu suất phản hồi cực nhanh | 💫 Hiệu ứng hình ảnh hiện đại |

---

## ✨ Tính Năng

### 🎨 **Môi Trường Desktop**
- ✅ Hai tùy chọn compositor Wayland hiện đại (Niri/Hyprland)
- ✅ Giao diện shell đẹp mắt và chức năng (DMS/Caelestia)
- ✅ Theme GTK/Qt hoàn chỉnh với nhiều bộ icon
- ✅ Bộ sưu tập hình nền tùy chỉnh
- ✅ Hệ thống thông báo chuyên nghiệp (Mako cho Niri)

### 🚀 **Tối Ưu Hóa Hiệu Suất**
- ⚡ Tinh chỉnh CPU đặc thù cho AMD Ryzen 7 5800X
- ⚡ Tối ưu GPU NVIDIA RTX 3060 (không thay đổi driver)
- ⚡ Tinh chỉnh tham số kernel cho kiến trúc Zen 3
- ⚡ Tối ưu bộ lập lịch I/O (BFQ/none)
- ⚡ Tối ưu ngăn xếp mạng (BBR, CAKE)

### 🎮 **Môi Trường Gaming**
- 🎮 Thiết lập gaming hoàn chỉnh (Steam, Lutris, Heroic)
- 🎮 Proton-GE và Wine-Staging đã cấu hình
- 🎮 Tối ưu CPU governor với GameMode
- 🎮 Lớp phủ hiệu suất MangoHud
- 🎮 Hỗ trợ tay cầm Xbox (xpadneo)

### 🤖 **Phát Triển AI/ML**
- 🧠 CUDA 12.x với hỗ trợ cuDNN
- 🧠 PyTorch với tăng tốc CUDA
- 🧠 Ollama cho suy luận LLM cục bộ
- 🧠 Cấu hình lưu trữ model tùy chỉnh
- 🧠 Docker với NVIDIA Container Toolkit

### 💻 **Môi Trường Phát Triển**
- 🛠️ .NET 8.0 & 9.0 SDK
- 🛠️ Phụ thuộc Unreal Engine 5
- 🛠️ Docker & Docker Compose
- 🛠️ Nhiều IDE (Rider, VSCodium)
- 🛠️ Bộ công cụ build hoàn chỉnh (Clang, GCC, LLD)

### 🎨 **Bộ Công Cụ Sáng Tạo**
- 🎬 Chỉnh sửa video (Kdenlive, DaVinci Resolve)
- 🖼️ Chỉnh sửa hình ảnh (GIMP, Krita, Inkscape)
- 🎵 Sản xuất âm thanh (Audacity, Ardour)
- 🎥 Thiết lập streaming (OBS Studio với VA-API)
- 🧊 Tạo 3D (Blender với kết xuất GPU)

### 🌐 **Tính Năng Hệ Thống**
- 📡 Bộ gõ tiếng Việt (Fcitx5 + Bamboo)
- 🔒 DNS-over-TLS (Cloudflare + Quad9)
- 🌐 Cấu hình IP tĩnh
- 🔐 Hệ thống sao lưu tự động
- 📊 Giám sát hệ thống toàn diện

---

## 💻 Yêu Cầu Hệ Thống

### Tối Ưu Cho
- **Hệ điều hành**: CachyOS (phiên bản mới nhất)
- **Bo mạch chủ**: ROG STRIX B550-XE GAMING WIFI
- **CPU**: AMD Ryzen 7 5800X (8C/16T)
- **GPU**: NVIDIA RTX 3060 12GB
- **RAM**: 32GB+ DDR4
- **Ổ cứng**: 50GB dung lượng trống (khuyến nghị 100GB+ cho AI/ML)

---

## 🚀 Cài Đặt Nhanh

### Cài Đặt Một Dòng Lệnh

```bash
curl -fsSL https://raw.githubusercontent.com/hoangducdt/Wayland/main/install.sh | bash
```

### Điều Gì Xảy Ra Trong Quá Trình Cài Đặt?

1. **Kiểm Tra Tiền Điều Kiện**: Xác thực quyền sudo và yêu cầu hệ thống
2. **Lựa Chọn Compositor**: Menu tương tác để chọn Niri hoặc Hyprland
3. **Cập Nhật Hệ Thống**: Cập nhật các gói và keyring của CachyOS
4. **Cài Đặt Gói**: Cài đặt hơn 200 gói đã được chọn lọc kỹ lưỡng
5. **Cấu Hình**: Tạo symlink cho tất cả file cấu hình
6. **Tối Ưu Hóa**: Áp dụng các tinh chỉnh đặc thù cho phần cứng
7. **Thiết Lập Dịch Vụ**: Kích hoạt và cấu hình các dịch vụ systemd
8. **Tạo Bản Sao Lưu**: Sao lưu các cấu hình hiện có

**Tổng Thời Gian Cài Đặt**: ~30-60 phút (tùy thuộc tốc độ internet)

---

## 📋 Các Bước Sau Cài Đặt

### 1. **Khởi Động Lại Hệ Thống**
```bash
sudo reboot
```
**Tại sao?** Áp dụng các module kernel, cài đặt NVIDIA và dịch vụ hệ thống.

### 2. **Chọn Compositor Của Bạn Tại Màn Hình Đăng Nhập**
- Chọn **Niri** hoặc **Hyprland** từ menu phiên GDM
- Lựa chọn của bạn được lưu cho các lần đăng nhập sau

### 3. **Cấu Hình Fcitx5 (Bộ Gõ Tiếng Việt)**
```bash
# Mở Cấu hình Fcitx5
fcitx5-configtool
```
- Thêm phương thức nhập "Bamboo"
- Đặt phím chuyển đổi (mặc định: Ctrl+Space)

### 4. **Kiểm Tra Driver NVIDIA**
```bash
nvidia-smi
```
Kết quả mong đợi: Thông tin GPU, phiên bản driver, phiên bản CUDA

### 5. **Khởi Động Ollama Cho AI/ML** (Tùy chọn)
```bash
sudo systemctl start ollama
ollama run llama3.2
```

### 6. **Cấu Hình IP Tĩnh** (Nếu cần)
Chỉnh sửa `/etc/NetworkManager/system-connections/static-ethernet.nmconnection`
```ini
[ipv4]
method=manual
address1=IP_CỦA_BẠN/24,GATEWAY_CỦA_BẠN
dns=1.1.1.1;1.0.0.1;
```

### 7. **Cài Đặt Font Bổ Sung** (Tùy chọn)
```bash
yay -S ttf-ms-fonts noto-fonts-cjk
```

### 8. **Tùy Chỉnh Theme**
- **GTK**: Sử dụng `nwg-look` 
- **Qt5/Qt6**: Sử dụng `qt5ct` và `qt6ct`
- **Icons**: Nhiều bộ đã cài đặt sẵn (Papirus, Tela, WhiteSur)

---

## 📦 Nội Dung Bao Gồm

<details>
<summary><b>🖥️ Hệ Thống Cốt Lõi (Nhấp để mở rộng)</b></summary>

- **Display Server**: Wayland với hỗ trợ XWayland
- **Login Manager**: GDM với theme tùy chỉnh
- **Trình quản lý file**: Thunar với hỗ trợ nén
- **Terminal**: Kitty (tăng tốc GPU)
- **Shell**: Fish với Starship prompt
- **Mạng**: NetworkManager + iwd
- **Bluetooth**: Bluez + Blueman

</details>

<details>
<summary><b>🎨 Thành Phần Desktop</b></summary>

**Cho Niri:**
- Niri compositor
- DankMaterialShell (DMS)
- Thông báo Mako
- Swaybg, Swaylock, Swayidle

**Cho Hyprland:**
- Hyprland compositor
- Caelestia shell (dựa trên QuickShell)
- Trình quản lý phiên UWSM
- XDG portal đặc thù cho Hyprland

**Chung:**
- Fuzzel launcher
- Cliphist clipboard manager
- Hyprpicker color picker
- Brightnessctl điều khiển độ sáng
- Nhiều bộ sưu tập hình nền

</details>

<details>
<summary><b>🎮 Gaming & Giải Trí</b></summary>

- **Nền tảng**: Steam, Lutris, Heroic Games Launcher
- **Tương thích**: Wine-Staging, Proton-GE, DXVK
- **Công cụ**: MangoHud, GameMode, Gamescope
- **Tay cầm**: xpadneo (Xbox), hỗ trợ HID chung
- **Giả lập**: Sẵn sàng cài đặt giả lập

</details>

<details>
<summary><b>💻 Công Cụ Phát Triển</b></summary>

- **Trình soạn thảo**: Neovim, VSCodium, Kate
- **IDE**: JetBrains Rider
- **Ngôn ngữ**: .NET 8/9, Node.js, Rust, Go, Python 3.x
- **Quản lý phiên bản**: Git, Git LFS, GitHub CLI/Desktop
- **Container**: Docker, Docker Compose
- **Cơ sở dữ liệu**: PostgreSQL, Redis
- **Công cụ build**: CMake, Ninja, Meson, ccache

</details>

<details>
<summary><b>🤖 Môi Trường AI/ML</b></summary>

- **Framework**: PyTorch (CUDA), TensorFlow
- **CUDA**: CUDA Toolkit 12.x, cuDNN
- **Suy luận**: Ollama với lưu trữ model tùy chỉnh
- **Thư viện**: NumPy, Pandas, Scikit-learn, Transformers
- **Công cụ**: Jupyter Notebook, LM Studio
- **Docker**: NVIDIA Container Toolkit

</details>

<details>
<summary><b>🎨 Ứng Dụng Sáng Tạo</b></summary>

- **3D**: Blender (kết xuất GPU), Natron
- **Video**: Kdenlive, DaVinci Resolve, OBS Studio
- **Hình ảnh**: GIMP, Krita, Darktable, RawTherapee
- **Vector**: Inkscape
- **Âm thanh**: Audacity, Ardour, EasyEffects
- **Xuất bản**: Scribus

</details>

<details>
<summary><b>📊 Giám Sát Hệ Thống</b></summary>

- **CPU**: htop, btop, zenmonitor (AMD)
- **GPU**: nvtop, CoreCtrl
- **Mạng**: iftop, NetworkManager
- **Ổ đĩa**: GNOME Disks
- **Hệ thống**: fastfetch, lm_sensors

</details>

---

## ⚡ Tối Ưu Hóa Hệ Thống

### 🔧 Tối Ưu CPU (Ryzen 7 5800X)

```bash
# CPU Governor
- Chế độ hiệu suất cho sử dụng desktop
- Tự động cấu hình qua dịch vụ systemd

# Tham Số Kernel
vm.swappiness=10                    # Giảm thiểu sử dụng swap
vm.vfs_cache_pressure=50            # Áp lực cache cân bằng
vm.dirty_ratio=10                   # Tối ưu đệm ghi
net.core.default_qdisc=cake         # QoS mạng tốt hơn
net.ipv4.tcp_congestion_control=bbr # Thuật toán TCP hiện đại
```

### 🎮 Tối Ưu GPU (RTX 3060)

```bash
# Cấu Hình NVIDIA Modprobe
options nvidia_drm modeset=1 fbdev=1
options nvidia NVreg_PreserveVideoMemoryAllocations=1
options nvidia NVreg_UsePageAttributeTable=1
options nvidia NVreg_DynamicPowerManagement=0x02

# Module Khởi Động Sớm
MODULES=(nvidia nvidia_modeset nvidia_uvm nvidia_drm)

# Tăng Tốc Video
- VA-API qua nvidia-vaapi-driver
- Giải mã/mã hóa video phần cứng
```

### 💾 Tối Ưu Lưu Trữ

```bash
# Bộ Lập Lịch I/O
- BFQ cho ổ đĩa quay (HDD)
- none cho SSD NVMe (tối ưu)

# Hệ Thống File
- Hỗ trợ Btrfs
- Đọc/ghi NTFS qua ntfs-3g
- Hỗ trợ exFAT cho ổ ngoài
```

### 🌐 Tối Ưu Mạng

```bash
# DNS
- Chính: Cloudflare (1.1.1.1, 1.0.0.1)
- Dự phòng: Quad9, Google DNS
- DNS-over-TLS đã bật

# Ngăn Xếp TCP
- Kiểm soát tắc nghẽn BBR
- Kỷ luật hàng đợi CAKE
```

### 🎵 Tối Ưu Âm Thanh

```bash
# Cấu Hình PipeWire
- Âm thanh độ trễ thấp
- Thay thế máy chủ âm thanh JACK
- Hỗ trợ Bluetooth
- EasyEffects cho xử lý âm thanh
```

---

## 📁 Cấu Trúc Thư Mục

```
~/.config/
├── niri/                      # Cấu hình Niri
├── hypr/                      # Cấu hình Hyprland
├── DankMaterialShell/         # Cấu hình DMS
├── caelestia/                 # Cấu hình Caelestia
├── kitty/                     # Cấu hình terminal
├── fish/                      # Cấu hình shell
├── fuzzel/                    # Cấu hình launcher
├── mako/                      # Cấu hình thông báo
├── btop/                      # Giám sát hệ thống
├── fastfetch/                 # Thông tin hệ thống
└── gtk-3.0/                   # Theme GTK

~/.local/share/Wayland/        # File cài đặt
├── Configs/                   # Tất cả file cấu hình
└── install.sh                 # Script cài đặt
```

---

## 🛠️ Hướng Dẫn Tùy Chỉnh

### Thay Đổi Hình Nền

**Niri:**
```bash
# Chỉnh sửa ~/.config/niri/config.kdl
outputs {
    "DP-1" {
        background-path "/đường/dẫn/tới/hình-nền.jpg"
    }
}
```

**Hyprland:**
```bash
# Chỉnh sửa ~/.config/hypr/hyprland/hyprland.conf
exec-once = swaybg -i /đường/dẫn/tới/hình-nền.jpg
```

### Tùy Chỉnh Phím Tắt

**Niri:** Chỉnh sửa `~/.config/niri/config.kdl` trong phần `binds`

**Hyprland:** Chỉnh sửa `~/.config/hypr/hyprland/keybindings.conf`

### Thay Đổi Theme Shell

**DMS:** Cấu hình trong `~/.config/DankMaterialShell/`

**Caelestia:** 
```bash
caelestia-cli theme list
caelestia-cli theme set <tên-theme>
```

### Sửa Đổi Giám Sát Hệ Thống

```bash
# Chỉnh sửa cấu hình btop
micro ~/.config/btop/btop.conf

# Chỉnh sửa cấu hình fastfetch
micro ~/.config/fastfetch/config.jsonc
```

---

## 📚 Các Lệnh Hữu Ích

### Quản Lý Hệ Thống

```bash
# Cập nhật hệ thống
sudo pacman -Syu

# Dọn dẹp bộ nhớ cache gói
sudo paccache -r

# Kiểm tra log hệ thống
journalctl -xb

# Giám sát tài nguyên hệ thống
btop
```

### Điều Khiển Compositor

**Niri:**
```bash
# Tải lại cấu hình
niri msg reload-config

# Thoát compositor
niri msg exit
```

**Hyprland:**
```bash
# Tải lại cấu hình
hyprctl reload

# Lấy thông tin cửa sổ đang hoạt động
hyprctl activewindow

# Liệt kê workspace
hyprctl workspaces
```

### Docker

```bash
# Khởi động dịch vụ Docker
sudo systemctl start docker

# Chạy với hỗ trợ GPU
docker run --gpus all nvidia/cuda:12.0-base nvidia-smi

# Docker Compose
docker-compose up -d
```

### AI/ML (Ollama)

```bash
# Khởi động dịch vụ Ollama
sudo systemctl start ollama

# Chạy một model
ollama run llama3.2

# Liệt kê model đã cài
ollama list

# Tải model mới
ollama pull codellama
```

### Gaming

```bash
# Chạy game với MangoHud
mangohud %command%

# Chạy với GameMode
gamemoderun %command%

# Kiểm tra phiên bản Proton
ls ~/.steam/steam/compatibilitytools.d/
```

---

## 🐛 Khắc Phục Sự Cố

### Vấn Đề Driver NVIDIA

**Vấn đề:** Màn hình đen sau khi cài đặt

**Giải pháp:**
```bash
# Khởi động vào TTY (Ctrl+Alt+F2)
sudo systemctl disable gdm
sudo mkinitcpio -P
sudo systemctl enable gdm
sudo reboot
```

### Quyền Truy Cập Docker Bị Từ Chối

**Vấn đề:** `permission denied while trying to connect to the Docker daemon`

**Giải pháp:**
```bash
# Đăng xuất và đăng nhập lại
# Hoặc kích hoạt nhóm thủ công
newgrp docker
```

### Lưu Trữ Model Ollama

**Vấn đề:** Không tìm thấy model hoặc vấn đề lưu trữ

**Giải pháp:**
```bash
# Kiểm tra thư mục model
ls ~/AI-Models/ollama/

# Xác minh dịch vụ Ollama
sudo systemctl status ollama

# Kiểm tra biến môi trường
sudo systemctl cat ollama | grep OLLAMA_MODELS
```

### Compositor Không Khởi Động

**Vấn đề:** Compositor crash khi khởi động

**Giải pháp:**
```bash
# Kiểm tra log
journalctl --user -u niri -b
# hoặc
journalctl --user -u hyprland -b

# Xác minh phiên Wayland
echo $XDG_SESSION_TYPE
```

### Bộ Gõ Tiếng Việt Không Hoạt Động

**Vấn đề:** Fcitx5 Bamboo không phản hồi

**Giải pháp:**
```bash
# Khởi động lại Fcitx5
killall fcitx5
fcitx5 -d

# Kiểm tra biến môi trường trong cấu hình shell
echo $GTK_IM_MODULE
echo $QT_IM_MODULE
echo $XMODIFIERS
```

### Vấn Đề Âm Thanh

**Vấn đề:** Không có âm thanh hoặc âm thanh bị rè

**Giải pháp:**
```bash
# Khởi động lại PipeWire
systemctl --user restart pipewire pipewire-pulse wireplumber

# Kiểm tra thiết bị âm thanh
pactl list sinks

# Xác minh định tuyến âm thanh
helvum
```

---

## 📊 Đánh Giá Hiệu Suất

### Thời Gian Khởi Động Hệ Thống
- **Mục tiêu**: < 15 giây đến màn hình đăng nhập
- **Khởi động Compositor**: < 3 giây

### Sử Dụng Tài Nguyên (Idle)

| Compositor | RAM | CPU | GPU VRAM |
|------------|-----|-----|----------|
| Niri + DMS | ~1.2GB | 2-3% | ~400MB |
| Hyprland + Caelestia | ~1.5GB | 3-5% | ~600MB |

### Hiệu Suất Gaming
- **GameMode**: Tăng +5-15% FPS
- **MangoHud**: Ảnh hưởng hiệu suất < 1%
- **Tương thích Proton**: 95%+ thư viện Steam

---

## 🔐 Tính Năng Bảo Mật

- ✅ Mã hóa DNS-over-TLS
- ✅ Sao lưu hệ thống tự động
- ✅ GNOME Keyring để quản lý mật khẩu
- ✅ Agent xác thực Polkit
- ✅ Firewall sẵn sàng (cấu hình theo nhu cầu)
- ✅ Tương thích Secure boot (module NVIDIA đã ký)

---

## 📝 Ghi Log & Sao Lưu

### Log Cài Đặt
```bash
~/setup_complete_YYYYMMDD_HHMMSS.log    # Log cài đặt chính
~/setup_errors_YYYYMMDD_HHMMSS.log      # Log lỗi
~/install-summary.txt                    # Tóm tắt cài đặt
```

### Sao Lưu Cấu Hình
```bash
~/Documents/wayland-configs-YYYYMMDD_HHMMSS/  # Cấu hình đã sao lưu
```

### Quản Lý Trạng Thái
```bash
~/.cache/wayland-setup/setup_state.json  # Theo dõi trạng thái cài đặt
```

---

## 📜 Giấy Phép

Dự án này được cấp phép theo Giấy phép MIT - xem file [LICENSE](LICENSE) để biết chi tiết.

---

<div align="center">

**Made with ❤️ for ROG STRIX B550-XE | Ryzen 7 5800X | RTX 3060 12GB**

**Ready to game, develop, create, and render! 🚀🎮💻🎨**

[⬆ Về Đầu Trang](#wayland-dotfiles---cấu-hình-tối-ưu-cho-cachyos)

</div>