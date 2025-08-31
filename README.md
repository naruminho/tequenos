# Tequenos - Grid Editor v3

A minimal grid editor written in **vanilla JavaScript**, with **no external dependencies**.  
It runs fully **offline**, directly in your browser.  
Perfect for creating pixel-style drawings, assembling Tetris-like pieces, and saving/loading your work in JSON.

## ✨ Features
- **Drawing on a math-paper style grid**
- **Editing tools**:
  - ✏️ **Draw** – paint cells with the selected color
  - 🧽 **Erase** – clear cells
  - 👆 **Select** – select and move objects
- **Connected objects**:
  - Cells connected horizontally or vertically belong to the same object.
  - Diagonal connections do **not** count.
  - Inner shapes (a square inside another with empty space in between) are treated as separate objects.
- **Object text**: add labels to objects, edit inline with double click.
- **Object info panel**: see cell count, color, and text of the selected object.
- **Save & Load JSON** – export your drawing, reload it later.
- **Zoom and Pan** support for large grids.
- **Built-in usage instructions** in the UI.

## 🚀 How to Run
1. Open `grid-editor-v3.html` in your browser.  
   *(No installation, no server, no npm required)*  
2. Use the top toolbar to select tools:
   - **Draw**: click & drag to paint.
   - **Erase**: click to clear.
   - **Select**: click an object to select, move, or edit it.
3. Use mouse wheel to **zoom**, drag the background to **pan**.
4. Click **💾 Save** to export as JSON, and **📁 Load** to reload.
5. **Double-click** object text to edit inline.

## 📂 JSON Structure
The exported file looks like this:
```json
{
  "gridState": { "row-col": "color", "...": "..." },
  "objects": [
    {
      "id": 123456,
      "cells": [{"row": 1, "col": 2}, {"row": 1, "col": 3}],
      "color": "#ff0000",
      "text": "My block",
      "bounds": {"minRow": 1, "maxRow": 1, "minCol": 2, "maxCol": 3}
    }
  ],
  "gridWidth": 100,
  "gridHeight": 100,
  "version": "3.0"
}
