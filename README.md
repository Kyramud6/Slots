# Canvas-Based UI Automation Project

## Project Overview
This project demonstrates a custom-built automation engine designed to interact with complex web environments where traditional DOM-based automation (Selenium/Playwright) is restricted. 

Developed during my QA internship, this tool solves the "Invisible Element" problem common in Canvas-rendered web applications by leveraging Computer Vision and Optical Character Recognition (OCR).

## The Technical Challenge
The target environment renders its UI via an HTML5 `<canvas>` element. This creates a "Black Box" scenario for QA:
* **Zero DOM Visibility:** No inspectable HTML elements (buttons, text fields, or labels).
* **Dynamic Content:** Real-time updates within the canvas that cannot be captured via standard event listeners.
* **Backend Isolation:** Interacting with the UI without direct API hooks.

## The Solution (Architecture)
To bypass these limitations, I using the tech below: 

1. **Optical Character Recognition (OCR):** Utilized `Tesseract OCR` to extract live data directly from the canvas pixels, allowing the script to "read" the application state.
2. **Pixel-Mapping Logic:** Implemented `PyAutoGUI` to handle precise user-input simulation (clicks/typing) based on visual triggers.
3. **Image Pre-processing:** Used the `Pillow` library to enhance screenshot contrast, significantly increasing OCR accuracy for stylized fonts.

## 📈 Key Learning Outcomes
* **Computer Vision in QA:** Successfully implemented non-standard testing methods for inaccessible UIs.
* **Error Handling:** Developed robust retry-logic to account for OCR "hallucinations" and lag in canvas rendering.
* **Strategic Workarounds:** Proved that automation is possible even when the underlying technology (Canvas/PHP) hides the source code.

---
*Note: This repository serves as a conceptual portfolio of my work. The source code is currently restricted to prevent unauthorized distribution.*
