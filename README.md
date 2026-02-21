
# Waybar Configuration

This repository contains the configuration files for **Waybar**, a customizable status bar for Wayland compositors like Hyprland and Sway.

## Prerequisites

Before using this configuration, ensure you have the following installed:

* **Waybar**: The status bar itself.
* **PipeWire**: Recommended for modern Bluetooth and audio handling.
* **Icon Fonts**: Required to display glyphs (Bluetooth, Battery, etc.) correctly.

<<<<<<< HEAD
The `Hack Nerd` package is required to display icons correctly in Waybar. Please make sure it is installed on your system.

Also make sure the session user is in the input group
## Steps
- Install dependencies while inside the cloned waybar directory "node scss compiler"   ` npm i `
- Run this command to compiles scss to css ` npx node-sass style.scss style.css 
 `
=======
  * `otf-font-awesome` (Font Awesome 6)
  * `ttf-nerd-fonts-symbols-common` (Nerd Font Symbols)
* **Node.js & NPM**: Required for the SCSS compiler.

> **Note:** Ensure your session user is in the `input` and `video` groups to allow Waybar to access backlight and input device information.

---

## Installation & Setup

### 1. Install Dependencies

Navigate into your cloned Waybar configuration directory and install the necessary Node modules:

```bash
npm install
```

---

### 2. Compile SCSS to CSS

This configuration uses SCSS for styling. To compile the `.scss` file into the `.css` file that Waybar reads, use the modern Dart Sass compiler:

```bash
# Run the compiler
npx sass style.scss style.css
```

> **Note:** Do not use `node-sass`, as it is deprecated and does not support modern Node.js environments.

---

### 3. Configure Fonts

Ensure your `style.css` (or `style.scss` before compiling) includes the correct font families for your icons:

```css
* {
    /* Use Nerd Font symbols as a fallback for your main font */
    font-family: "Symbols Nerd Font", "Font Awesome 6 Free", Roboto, sans-serif;
    font-size: 13px;
}
```

---

### 4. Apply Changes

To apply your configuration, kill any running instances and restart Waybar:

```bash
# Apply the new configuration
killall waybar && waybar &
```

---

## Troubleshooting

If icons still appear as squares (missing glyphs), refresh your system font cache and verify the font names:

```bash
# Refresh system font cache
sudo fc-cache -fv

# Verify installed Nerd Fonts
fc-list | grep -i "nerd"
```

>>>>>>> 890cacb (update styling and fonts)
