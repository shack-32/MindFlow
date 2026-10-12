# MindFlow ✦ Studio Mind Mapping for Educational Videos

A high-aesthetic, lightning-fast mind mapping and visual concept canvas built specifically for **educators, video creators, course instructors, and visual presenters**.

Inspired by the fluidity of **XMind**, the infinite visual freedom of **Miro**, and the structured speed of **MindMup** — built with zero bloat and 100% local privacy.

---

## 🚀 How to Run

### Option 1: Double-Click (Zero Setup / Instant)
Simply double-click [`index.html`](./index.html) in your Windows File Explorer to open it directly in Chrome, Edge, Brave, or Firefox. No installation or internet server required.

### Option 2: Local Web Server
```bash
npm start
```
Then visit `http://localhost:3000`.

---

## ✨ Latest Enhancements & Fixes

### 1. 📐 Collision-Free Auto Spacing
- Upgraded the hierarchical tree layout engine with **dynamic branch span calculation** and an inter-branch isolation buffer (`SUBTREE_MARGIN = 56px`, `GAP_X = 140px`, `GAP_Y = 36px`).
- Boxes will **never touch or overlap**, and subtrees flow with generous breathing room.
- Relationship lines have increased curvature so their label pills never collide with or hide behind cards.

### 2. 🔲 Boundaries (Group Enclosures / Frames)
- Select one or more nodes and click the **Boundary** tool (or press **`B`**, or right-click -> **Create Boundary**).
- Wraps the member nodes in a sleek, tinted group container with customizable title tag, dashed border, and color accent.
- Boundaries dynamically re-bound and expand as your diagram evolves. Double-click the boundary label to rename it!

### 3. 🖱️ Laptop Trackpad Two-Finger Navigation (Pan vs Zoom)
- **Two-finger slide** on your trackpad fluidly **pans** up, down, left, and right (like Miro, Google Maps, and Figma).
- **Pinch-to-zoom** (or `Ctrl + Mouse Wheel`) zooms in/out smoothly centered at your cursor.

### 4. 🧰 Mouse Tools & Marquee Box Selection
- **Select Tool (`V`)**: Single click to select, or drag on the empty canvas to draw a **Marquee Selection Box** to multi-select nodes.
- **Hand Tool (`H`)**: Drag anywhere to pan the canvas.
- **Arrow Tool (`C`)**: Click from node to node to draw curved relationship arrows.
- **Boundary Tool (`B`)**: Wrap selected nodes into a boundary group.

### 5. 📋 Right-Click Context Menu
- Right-click any topic to open a glassmorphism menu:
  - Add Subtopic (`Tab`)
  - Add Sibling Topic (`Enter`)
  - Connect Arrow (`C`)
  - Create Boundary (`B`)
  - Edit Details & Notes
  - Duplicate Branch (`Ctrl+D`)
  - Fold / Unfold (`Space`)
  - Delete Topic (`Del`)
- Right-click canvas to create topics, boundaries, or fit view.

### 6. 🔘 Centered Fold/Unfold Button with Auto-Hide
- The collapse/maximize circular button now uses **crisp, mathematically centered vector SVGs** for `+` and `−`.
- **Auto-hides** when the branch is expanded, only appearing when you hover over the node.
- If a branch is collapsed, the button stays visible with a distinct glowing accent indicator so you always know hidden subtopics are stored there.

### 7. 🎬 Presenter Mode Relationship Isolation
- When Presenter Spotlight Mode (`P`) is active, background relationship lines and label pills are dimmed out to 5% opacity.
- A relationship arrow and its label only shine at full brightness (`100%` spotlight) when the active topic being presented is directly connected to it.

### 8. ✏️ Direct Double-Click Title & Subtext Editing
- **Double-click title**: Edit the main topic title inline. Pressing `Tab` or `Shift + Enter` seamlessly jumps right into editing/adding subtext!
- **Double-click subtext**: Edit existing lecture notes or subtext inline in place.
- **Add subtext**: Hover or select any node without subtext to see the subtle `+ Add subtext` button, or double-click to type immediately!
- Press `Enter` to save, `Escape` to cancel. Empty subtext cleans up automatically.

### 9. 🧭 Real-Time Minimap Click-and-Drag Panning
- Hold and drag anywhere inside the bottom-right **Minimap Radar** to pan the camera smoothly across the canvas in real time.
- Upgraded `#minimap-canvas` with High-DPI (`devicePixelRatio`) Retina rendering and expanded overview bounds.

### 10. 🔌 Smart 4-Side Connector Pinning & Draggable Endpoints
- **Automatic Nearest-Side Pinning**: In Freeform Canvas, branch connectors automatically pin to the most intuitive side (`top`, `right`, `bottom`, or `left`) based on relative card positions (e.g. a subtopic placed above its parent pins from the parent's `top` edge to the subtopic's `bottom` edge).
- **Interactive Endpoint Handles**: Hover or click any connector line to reveal draggable circular handles at both the parent and child ends. Drag either endpoint to manually pin it to the `top`, `right`, `bottom`, or `left` port of its card with live magnetic snap guides.
- **Interactive Curve Shaping**: Drag the middle of any connector line to bend its Bezier curve, or double-click / press `Delete` on a selected connector to reset it to automatic routing.

### 11. ✨ Crisp High-DPI Vector Rendering at All Zoom Levels
- Eliminated Chromium GPU compositor texture freezing (`will-change` / `backdrop-filter`) and fractional `0.5px` sub-pixel card offsets so all cards, typography, borders, and SVG curves remain razor-sharp up to `350%` zoom without needing to click elements after zooming.

---

## ⌨️ Complete Keyboard Shortcuts Reference

| Shortcut | Action |
| :--- | :--- |
| **`V`** | Select Tool / Marquee Box Select |
| **`Tab`** | Add Subtopic (Child node) |
| **`Enter`** | Add Sibling Topic (at the same level) |
| **`B`** | Create Boundary around selected nodes |
| **`C`** | Connect Relationship Arrow |
| **`Delete`** / **`Backspace`** | Delete selected topic, arrow, or boundary |
| **`Double Click`** / **`F2`** | Edit topic title in place |
| **`Ctrl + D`** | Duplicate Topic & Subtree |
| **`Ctrl + F`** | Spotlight Search topics & notes |
| **`Ctrl + A`** | Select All visible topics |
| **`P`** | Toggle Presenter / Spotlight Mode |
| **`→` / `←`** | Next / Previous topic in presentation |
| **`Space`** | Fold / Unfold active branch |
| **`F`** | Fit entire mind map to view |
| **`Slide 2 fingers`** | Pan canvas up/down/left/right |
| **`Pinch / Ctrl+Wheel`** | Smooth zoom focused at cursor |
| **`Ctrl + Z` / `Ctrl + Y`** | Undo / Redo |
| **`?`** | Open Shortcuts cheat sheet |

---

## 💾 Export & Import Options

- **Save Project (`.json`)**: Exports your complete project including all sheets, topics, notes, relationships, boundaries, and colors.
- **Import Project (`.json`)**: Open previously saved `.json` maps, or simply **drag-and-drop** any saved `.json` file directly onto the canvas.
- **Export 4K PNG (Studio)**: Generates razor-sharp raster graphics with clean studio styling ready for YouTube thumbnails, video slides, or B-roll.
- **Export 4K PNG (Transparent)**: Transparent background PNG ready to drop over video footage as an overlay.
- **Export Scalable Vector (`.svg`)**: Clean SVG vector graphic for Premiere Pro, After Effects, DaVinci Resolve, or Illustrator.
- **Export Markdown Outline**: Clean indented markdown outline, perfect for course syllabi, video descriptions, or lecture notes.
- **Auto-Save**: Everything you create is automatically saved in your browser's local storage so you never lose your work on page refresh.
