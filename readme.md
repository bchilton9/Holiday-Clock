![License](https://img.shields.io/github/license/bchilton9/holiday-clock)
![Last Commit](https://img.shields.io/github/last-commit/bchilton9/holiday-clock)
![HTML5](https://img.shields.io/badge/Made%20with-HTML5-e34f26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-f7df1e?logo=javascript&logoColor=black)

# 🎉 Holiday Clock
A festive, self-contained clock designed for Raspberry Pi touchscreens and cheap TFT displays.

This single-file HTML clock automatically themes itself based on upcoming holidays, displays accurate countdowns, and features animated holiday characters that run across the screen. Optimized for small, low-quality displays with high-saturation colors and large, readable text.

___

## ✨ Features
- **Automatic holiday detection** — Activates 2 weeks before each holiday
- **Dynamic color themes** — Cycles through vibrant, TFT-optimized colors for each holiday
- **Accurate countdowns** — Fixed day-counting logic ensures correct "days until" display
- **Animated characters** — SVG-based runners (turkey, Santa, pumpkin, bunny, etc.) that appear randomly
- **Touch-friendly testing** — Tap the countdown text to spawn a character on demand
- **Auto-scaling** — Adapts to any screen size, from 3.5" Pi displays to full desktop
- **Daily auto-refresh** — Reloads at midnight to keep countdowns accurate

___

## 🎃 Supported Holidays
- 🎆 New Year's Day
- 💝 Valentine's Day  
- 🍀 St. Patrick's Day
- 🐰 Easter
- 🇺🇸 Memorial Day
- 🎆 4th of July
- 🛠️ Labor Day
- 🎃 Halloween
- 🦃 Thanksgiving
- 🎅 Christmas

___

## 🚀 Quick Start

### For Raspberry Pi / GitHub Pages
1. Download `index.html` from this repo
2. Upload to your web server or GitHub Pages
3. Open in a browser (fullscreen recommended)
4. **Optional:** Set your Pi to auto-launch the page on boot

### Local Testing
Simply open `index.html` in any modern browser. No server required!

___

## 🎨 Customization

### Adjusting Colors
Edit the `THEME` object around line 150 to change holiday color schemes:
```javascript
thanksgiving: { 
  backgrounds: ["#D2691E","#FF8C00"], 
  texts: ["#FFFF00","#FFFFFF"] 
}
```

### Changing Runner Size
Modify the `.runner` CSS around line 95:
```css
.runner {
  height: 70vh;  /* 70% of screen height - adjust as needed */
}
```

### Holiday Window Duration
Change `PRE_WINDOW_MS` around line 126 (default: 2 weeks):
```javascript
const PRE_WINDOW_MS = 14 * 24 * 60 * 60 * 1000; // milliseconds
```

___

## 📱 Touch Testing
On mobile or Pi touchscreen:
- **Tap the countdown text** (e.g., "1 day until Thanksgiving")
- **Tap the holiday message** (e.g., "Happy Thanksgiving!")

A character will immediately run across the screen!

___

## 🛠️ Technical Details
- **Pure HTML/CSS/JS** — No dependencies, frameworks, or build tools
- **SVG characters** — Crisp at any resolution, no sprite sheets needed
- **Responsive design** — Auto-scales based on viewport dimensions
- **Optimized for cheap TFT screens** — High saturation colors that won't wash out
- **Holiday calculations** — Handles movable holidays (Easter, Thanksgiving, etc.) correctly

___

## 🐛 Troubleshooting

**Countdown is off by a day?**  
The code now uses midnight-to-midnight calculations for accuracy. Make sure your system time is correct.

**Colors look washed out?**  
Adjust the `THEME` colors to higher saturation values. Cheap TFT displays often need brighter colors than monitors.

**Runners too small/large?**  
Change the `.runner` CSS `height` property (currently `70vh`).

**Holiday not activating?**  
Check that you're within 2 weeks before the holiday date. The clock uses the current system date.

___

## 📜 License
MIT – free to use and modify. Perfect for Raspberry Pi projects, kiosks, or just keeping track of the holidays!

___

## 🛠 Made By
[ChilSoft.com](https://chilsoft.com) — one turkey at a time. 🦃

___

## ⚠️ Disclaimer
This project is provided for informational and educational purposes only.  
Use any code or instructions at your own risk.  
We are **not responsible** for any damage to your device, data loss, or unintended consequences.  
Always proceed with care — and make backups.

© **2025 ChilSoft**. All rights reserved.