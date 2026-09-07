<div align="center">
# ASCII-Video
**Open-source real-time webcam-to-ASCII art converter.**
Transforms live video feeds into dynamic ASCII characters using browser-based image processing and canvas manipulation.
[Source](https://github.com/ruthwwikreddy/ascii-video) · Built by [Ruthwik Reddy](https://www.ruthwikreddy.live/)
MIT licensed · Client-side execution · No backend required
</div>

---

## Table of contents
1. [What ASCII-Video does](#1-what-ascii-video-does)
2. [How it Works](#2-how-it-works)
3. [Quick start](#3-quick-start)
4. [Features](#4-features)
5. [Technical details](#5-technical-details)
6. [Contributing](#6-contributing)
7. [License](#7-license)

---

## 1. What ASCII-Video does

| Capability | Detail |
|---|---|
| **Real-time Conversion** | Processes webcam frames instantly into ASCII characters using requestAnimationFrame. |
| **Client-side Privacy** | All processing happens locally in the browser; no video data is ever sent to a server. |
| **Dynamic Styling** | Support for multiple character sets (Elite, Soft, Binary) to change the aesthetic. |
| **Snapshot Capture** | Ability to freeze and save the current ASCII frame as a PNG image. |
| **Adaptive Contrast** | Invert mode and contrast adjustments to handle different lighting conditions. |

## 2. How it Works

```
Webcam Feed   ──▶   Canvas Sampling   ──▶   Luminance Calculation   ──▶   Character Mapping   ──▶   DOM Rendering
(MediaStream)      (Downsampled pixels)      (0-255 Gray scale)        (Value ➜ Char)          (HTML/CSS)
```

The system captures a frame from the webcam, calculates the brightness (luminance) of each pixel block, and maps that brightness to a specific character from a chosen set (e.g., `@` for dark, `.` for light).

## 3. Quick start

Since this is a frontend-only project, no installation is required.

1. **Clone the repository**:
   ```bash
   git clone https://github.com/ruthwwikreddy/ascii-video.git
   cd ascii-video
   ```

2. **Launch the app**:
   Open `index.html` in any modern web browser (Chrome, Firefox, Edge).

3. **Grant Permission**:
   Allow the browser to access your camera when prompted.

## 4. Features

- **Multiple Character Sets**: Choose between different ASCII styles to get varying levels of detail.
- **Resolution Control**: Adjust the sampling rate to create a "lo-fi" or "high-def" ASCII effect.
- **Invert Mode**: Instantly toggle between light and dark themes.
- **PNG Export**: Save your ASCII art directly to your device.

## 5. Technical details

- **Frontend**: Vanilla JavaScript, HTML5 Canvas, CSS3.
- **Performance**: Uses an off-screen canvas for pixel data sampling to maintain a high frame rate.
- **Styling**: Implements a modern glassmorphism UI for a professional user experience.

## 6. Contributing
Contributions are welcome! If you have a new character set or a performance optimization, feel free to open a Pull Request.

## 7. License
Released under the **MIT License** — feel free to use, modify, and distribute it.
