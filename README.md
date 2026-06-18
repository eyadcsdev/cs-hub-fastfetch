# CS HUB Fastfetch Themes

A curated collection of **Fastfetch themes** with image support and multiple layout styles, designed for a modern and clean terminal experience.

This project provides **8 themes**, each with **2 different layouts** (`sample_1` and `sample_2`), along with an **interactive installer** that lets you choose a theme and layout easily.

---

# ✨ Features

* 🎨 **8 Themes** with unique background images
* 🧩 **2 Layout Styles per theme**

  * `sample_1` → Compact layout
  * `sample_2` → Extended layout
* 👀 **Screenshot preview** for every theme and layou
* ⚙️ **Interactive installer**
* 📁 Clean and portable configuration structure
* 🖥️ Optimized for wide terminals
* 🐧 Official support for **NixOS**
* 🔄 Re-run the installer anytime to switch themes

---

# 📸 Preview

Each theme includes screenshots for both layouts.

Below is an example preview. More screenshots are available in the `screenshots/` directory.

## CS_HUB – Sample 1

![cs-hub-sample\_1](screenshots/cs-hub-sample_1.png)

## CS_HUB – Sample 2

![cs-hub-sample\_2](screenshots/cs-hub-sample_2.png)

---

# 🎨 Available Themes

| Theme             | sample_1 | sample_2 |
| ----------------- | -------- | -------- |
| Dragonball        | ✔️       | ✔️       |
| Dragonball 2      | ✔️       | ✔️       |
| Onepeace          | ✔️       | ✔️       |
| Sasaki            | ✔️       | ✔️       |
| Misi              | ✔️       | ✔️       |
| CS HUB            | ✔️       | ✔️       |
| Abo Obida         | ✔️       | ✔️       |
| Cristiano Ronaldo | ✔️       | ✔️       |

---

# 🧩 Layout Styles Explained

## sample_1

Compact layout with tighter spacing and focused information blocks.

## sample_2

Extended layout with wider spacing and clearer section separation.

The background image remains the same — only the information layout changes.

---

# ✅ Requirements

To get the best experience, make sure you have:

* Linux system
* Fastfetch
* Kitty terminal (required for image rendering)
* Nerd Font (required for icons)

> ⚠️ Image rendering is not supported in all terminals.
>
> Kitty and similar GPU-accelerated terminals are required.

---

# 🐧 NixOS Installation

NixOS users should install the required dependencies through `configuration.nix`.

Add the following:

```nix
environment.systemPackages = with pkgs; [
  fastfetch
  kitty
];
```

Then rebuild your system:

```bash
sudo nixos-rebuild switch
```

---

# 🖥️ Installing Kitty Terminal

## Ubuntu / Debian

```bash
sudo apt update
sudo apt install -y kitty
```

## Arch Linux

```bash
sudo pacman -S kitty
```

## Fedora

```bash
sudo dnf install kitty
```

Run Kitty:

```bash
kitty
```

---

# Installing Nerd Font (Required)

Icons and box characters require a Nerd Font.

## Recommended Font

JetBrainsMono Nerd Font

## Install the font

```bash
mkdir -p ~/.local/share/fonts
cd ~/.local/share/fonts

wget https://github.com/ryanoasis/nerd-fonts/releases/latest/download/JetBrainsMono.zip

unzip JetBrainsMono.zip

fc-cache -fv
```

---

# Configure Kitty to use the font

```bash
mkdir -p ~/.config/kitty
nano ~/.config/kitty/kitty.conf
```

Add:

```text
font_family JetBrainsMono Nerd Font
```

Restart Kitty after saving.

---

# Verify font installation

```bash
echo "      "
```

If icons appear correctly, the font is set up properly.

---

# 🚀 Easy Installation (Recommended)

This project includes an interactive installer that handles the configuration process for you.

## 1️⃣ Clone the repository

```bash
git clone https://github.com/alhattami0/cs-hub-fastfetch.git

cd cs-hub-fastfetch
```

---

## 2️⃣ Run the installer

```bash
chmod +x install.sh

./install.sh
```

---

## 3️⃣ What the installer does

* Ensures required directories exist
* Verifies required dependencies
* Lets you select a theme
* Lets you select a layout style
* Displays a screenshot preview (when Kitty is available)
* Copies theme assets
* Applies the selected Fastfetch configuration

After installation, run:

```bash
fastfetch
```

---

# 📦 Dependency Handling

The installer no longer installs packages automatically.

If required dependencies are missing, it will display instructions explaining how to install them for your system.

For NixOS users, dependencies should always be managed through `configuration.nix`.

---

# 🖥️ Recommended Terminal Size

For best visual results:

* Minimum: 100×25
* Recommended: 120×30

---

# 📁 Project Structure

```text
cs-hub-fastfetch/
├── assets/        # Theme images
├── configs/       # Fastfetch configuration files
├── screenshots/   # Preview images for each theme/layout
├── install.sh     # Interactive installer
├── README.md
└── LICENSE
```

---

# 📝 Notes

* All configuration paths are relative, making them portable.
* You can re-run the installer at any time to switch themes or layouts.
* Screenshots are named to match their configuration files exactly.
* Kitty is recommended for the full visual experience.
* Fastfetch configuration files are installed into:

```text
~/.config/fastfetch/
```

---

# 📖 Learn More About Fastfetch

If you are new to Fastfetch, check out this detailed guide:

https://itsfoss.com/fine-control-fastfetch/

---

# 📜 License

This project is licensed under the MIT License.

---

Enjoy customizing your terminal 🚀

If you find this project useful, consider giving it a ⭐ on GitHub.
