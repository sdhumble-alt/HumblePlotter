# A Humble Quick Plot

A lightweight, interactive client-side graph builder designed for students to rapidly create, customize, and export math and science charts.

**Author:** Steven Humble

**Version:** V 1.3.0

**Build Date:** 09-24-2026

**License:** Free for educational use

---

## 1. Overview

**A Humble Quick Plot** is an interactive, single-file HTML5 Canvas graphing web application. It simplifies graph generation for STEM assignments by providing an intuitive direct-manipulation interface for plotting data directly onto a canvas, managing multiple series, formatting mathematical typography, calculating linear regressions, and exporting clean figures for lab reports and presentations.

---

## 2. Key Features

### 📊 Graph Types

* **Bar Chart:** Grouped and clustered bar layouts with dynamic category management.


* **Line Graph:** Multi-series connected line plots with point markers and color coordination.


* **Scatter Plot:** Discrete point mapping with distinct marker shapes per series and automatic best-fit line regression.


* **Histogram:** Distribution graphing with custom bin starting points, bin widths, bin counts, and direct-click frequency entry.



### 🎨 Accessible Color System (Okabe-Ito Palette)

Pre-configured with universal colorblind-friendly colors:

1. **Navy / Blue** (`#0072B2`)


2. **Orange** (`#E69F00`)


3. **Bluish Green** (`#009E73`)


4. **Vermilion** (`#D55E00`)


5. **Sky Blue** (`#56B4E9`)


6. **Reddish Purple** (`#CC79A7`)


7. **Darkened Gold** (`#E5C494`)


8. **Charcoal Slate** (`#4A5568`)



* *Custom Hex Picker:* Allows picking any custom color via an integrated HTML color picker.



### 📐 Scientific & Math Tools

* **Linear Regression:** Automatic calculation and overlay of the slope-intercept equation ($y = mx + b$) and coefficient of determination ($R^2$) on scatter plots.


* **± Error Bars:** Interactive drag-to-set error bar sizing mode with horizontal end caps.


* **Quarter-Interval Minor Gridlines:** Toggleable subtle gridlines drawn at 1/4, 1/2, and 3/4 intervals between major scale ticks.


* **Adjustable Tick Font Size:** Numeric stepper control directly inside the Tools & Modifiers bar to adjust axis number and category label sizes (defaulting to 16px).
* **Scientific Symbols Dropdown:** Quick-insertion for `±`, `°`, `μ`, `Δ`, `Ψ`, `α`, `β`, `Φ`, and `×`.


* **One-Click Sub/Superscript:** `X²` and `X₂` buttons to transform highlighted text into native Unicode sub/super characters.



### 🔒 Contextual Workflow Locks

To prevent incomplete plots, interface controls dynamically unlock as required prerequisites are completed:

* **Bar Graph:** The "Groups within Categories" and "Labels & Scales" cards remain locked until at least one X category has been added.
* **Histogram:** The "Series" and "Labels & Scales" cards remain locked until all three bin parameters (*Bin Starts At*, *Width of Bin*, and *# of Bins*) have been entered.

### 💾 Project Management & Export

* **JSON Project Persistence:** Save (`.json`) and open complete project files to resume work across sessions. Saves graph type, labels, scale bounds, bin settings, tick font size, and plotted data.


* **Export Options:** Download high-resolution PNG images with an integrated legend strip, or copy the composite graphic directly to the system clipboard.



---

## 3. UI Layout & Controls Structure

### Left Panel: Step-by-Step Configuration Cards

1. **Graph Type:** Grid selector for Bar, Line, Scatter, and Histogram layouts.


2. **Tools & Modifiers:**
* **Action Grid:** Row 1 (*Best Fit*, *± Error*, *Minor Grid*); Row 2 (*Undo*, *Delete*, *Clear*).
* **Tick Font Stepper:** Numeric input box with native up/down increment arrows to control tick label size.


3. **X Categories (Bar Graph Only):** Input field, category chip tag list, and removal buttons.


4. **Histogram Bins (Histogram Only):** 3-column input configuration for *Bin Starts At*, *Width of Bin*, and *# of Bins*.
5. **Series / Groups within Categories:** Multi-series manager with individual color pickers, label renaming fields, and SVG trash-can deletion buttons.


6. **Labels & Scales:** Title, X/Y axis labels, symbol toolbar, formatting tools, and numeric scale ranges (Min, Max, Step).



### Right Panel: Interactive Canvas Stage

* **Active Drawing Strip:** Bar/Line series selection indicators.


* **HTML Legend Strip:** Dynamic color swatch and title summary.


* **Canvas Stage:** 3-layer HTML5 canvas viewport for real-time drafting and point placement.


* **Export Tray:** Action buttons to download PNG or copy image to clipboard.



---

## 4. Architecture & Technology

### Technology Stack

* **HTML5 Canvas:** 3-layer canvas stack (`gc` for grid/labels, `dc` for data points/lines, `oc` for overlays).


* **Vanilla JavaScript:** Zero external JavaScript dependencies; self-contained DOM manipulation and canvas rendering.


* **Tabler Icons & Inline SVG:** Used for clean, dependency-resilient UI icons.


* **CSS3:** Flexible split-view layout with custom form elements and focus rings.



### Canvas Layering Model

```text
┌───────────────────────────────────────────┐
│ #graph-wrap                               │
│  ├─ canvas #gc (Grid, Ticks, Axes, Titles)│
│  ├─ canvas #dc (Bars, Lines, Scatter, Fit)│
│  └─ canvas #oc (Interactive Overlays)     │
└───────────────────────────────────────────┘

```
