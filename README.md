# 🍱 Kawaii Bento Studio

An interactive, super-cute virtual lunchbox builder built to practice intermediate frontend engineering concepts. Drag, drop, rotate, and pack the perfect custom lunch!

---

## 🚀 Features

* **Multi-Compartment Tray:** A beautifully sectioned Bento box layout utilizing a custom CSS Grid template to separate your main meals, greens, and fruits.
* **Categorized Tab Navigation:** Instantly swap between different food groups (Meals, Greens, Fruits, Treats) with dynamic class switching.
* **Flawless Drag-and-Drop:** Powered by modern standard `PointerEvents` and `setPointerCapture` for pixel-perfect tracking on both desktop mice and mobile touchscreens.
* **Interactive Transforms:** Double-click any piece of food to rotate it by 45 degrees for that perfect, artistic packing layout.
* **Procedural Audio FX:** A custom Web Audio API synthesizer that procedurally generates a cute cartoon "plop" sound whenever an item is dropped.
* **Easy Removals:** Right-click (or long-press on mobile) any item to instantly delete it, or hit the "Eat Everything!" button to wipe the tray clean.

---

## 🛠️ Technologies Used

* **HTML5:** Semantic architecture, grid containers, and custom `data-*` attributes for state management.
* **CSS3:** * **CSS Grid & Flexbox:** Handling complex alignment for both the menu panels and the rigid box dividers.
    * **Mobile Optimizations:** Using `touch-action: none` to stop annoying browser window scrolling while dragging food around.
* **JavaScript (ES6):**
    * **Web Audio API:** Creating hardware-accelerated sound via custom `OscillatorNode` and `GainNode` pitch/volume ramps.
    * **DOM Manipulation:** High-efficiency element creation (`document.createElement`) and real-time bounding rect calculations (`getBoundingClientRect`).

---

## 📂 Code Design (Human-Centric Approach)

The logic is built to be simple, clean, and easy to read without unnecessary framework bloat:

* **`sound()`**: Fires up a brief, self-destroying audio context to synthesis a bouncy pitch signature.
* **`tab(id)`**: Clears previous active view states and triggers the visibility of the clicked category grid.
* **`drop(emoji)`**: The main engine. Spawns the element, tracks pointer position offsets, applies strict boundary limits to keep food inside the box, and attaches single-item event listeners.
* **`reset()`**: Selects all current food sticker nodes and purges them safely from the document tree.

---

## 📦 Getting Started

1. Save the codebase into a single file named `index.html`.
2. Double-click the file to open it directly in any modern web browser.
3. Start packing! To swap the emojis for custom hand-drawn `.png` assets later, simply change the text strings in the `drop()` triggers to your image file paths.
