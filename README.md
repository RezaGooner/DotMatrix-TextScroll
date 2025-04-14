# LED Matrix Scrolling

A simple AVR project that uses an **ATMega32** microcontroller to slowly scroll the name **"RezaGooner"** on an 8x8 LED Dot Matrix display from **right to left**.

## 📌 Project Goal

The goal of this project is to design and implement the hardware and software required to scroll a name (or any other text) on an 8x8 dot matrix using an AVR microcontroller. In this project, I have used "REZAGOONER" for the text, which you can implement to customize your own text with your own font.

---

## ⚙️ Hardware Components

- 1x8x8 LED Dot Matrix
- 1 x ATMega32 Microcontroller

---

## 🔌 Hardware Connections

- **PORTA** → Connects to **Columns** of Dot Matrix
- **PORTB** → Connects to **Rows** of Dot Matrix

Make sure the dot matrix wiring is aligned with the direction used in the software (horizontal movement requires proper row/column mapping).

---

## 🧠 Software Features

- Bitmapped characters are stored in hexadecimal arrays** by column.
- Scroll text **from right to left**, one column at a time.
- Delay added for smooth and readable movement.
- Efficient column shifting using bit manipulation.

---

## 🧪 Simulation

The circuit has been fully simulated and tested using **Proteus**.
- The compiled ".hex" file was loaded into the ATMega32.
- Proper behavior and text movement across the matrix display was visually verified.

---

## 💻 Code Overview

```c
char unsigned continue_text[] = {
// Hex codes for scrolling characters in "Reza Guner"
};
```

- PORTA controls the active column selection (~(1 << i))

- PORTB outputs the corresponding row pattern for each column.

- scroll_continuous_text() handles the animation by looping over all columns.

- A small delay ensures that each frame is displayed clearly.

---

## ▶️ How it works
The character bitmaps are predefined for the full name.

The microcontroller continuously scans and updates the display one column at a time.

For each change step, 8 columns are drawn sequentially to simulate motion.

The text appears to "scroll" slowly from right to left.


## Circuit

![bandicam2025-04-1023-52-28-650online-video-cutter com1-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/2dddaffb-658e-47f3-b75a-857849076e72)

![image](https://github.com/user-attachments/assets/33019c8f-a8af-4231-aecc-47db9ae17cb7)
