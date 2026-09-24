# A Humble Plotter

A lightweight, zero-backend graphing and data visualization web application designed for teachers, students, and scientists[cite: 1]. Built as a standalone HTML file with vanilla JavaScript, CSS3, Tabler Icons, and Chart.js[cite: 1].

---

## Overview

**A Humble Plotter** allows users to quickly format data, configure visual options, preview changes in real time, and export production-ready charts or tables[cite: 1]. The interface features an independent two-column split screen: the left pane handles graph selection, style settings, and data entry, while the right pane provides a live preview and quick-export controls[cite: 1].

* **Version**: 2.0.0[cite: 1]
* **Release Date**: 2026-09-22[cite: 1]
* **Author**: Steven Humble[cite: 1]
* **Tech Stack**: Vanilla HTML5, CSS3, JavaScript (ES6), Chart.js (v4.4.1), Tabler Icons (v3.31.0)[cite: 1].

---

## Features & Modules

### 1. Graph Types
* **Bar Chart**: Supports 1 to 5 grouped series per category, custom textures (solid, diagonal lines, light tint, crosshatch, sparse dots), error bars ($\pm$), and on-bar data labels[cite: 1].
* **Line Chart**: Multi-series line plots with configurable line styles (solid, dashed, dotted, dash-dot, long dash), custom node marker styles, dual Y-axis ($Y_2$) support, and point error bars[cite: 1].
* **Scatter Plot**: Numerical $XY$ plots supporting custom marker shapes, linear regression trendlines, independent $X$ and $Y$ error bars, and dual Y-axis ($Y_2$) support[cite: 1].
* **Histogram**: Frequency distributions with automatic bin calculation or custom start/bin widths, configurable bin boundary label styles, and diagonal/vertical label rotation[cite: 1].
* **Pie Chart**: Slice customization with interactive legends and flexible callout/slice labeling (percentages, raw counts, label names, or combinations)[cite: 1].
* **Box & Whisker**: Five-number summary visualization computed directly from raw data arrays, featuring configurable outlier handling (all values, 1.5 $\times$ IQR fence markers, or excluded outliers)[cite: 1].

### 2. Data Tools
* **Data Table**: Canvas-rendered tabular data generator with custom fonts, border styling, header shading, cell alignments, alternating row backgrounds, and direct CSV/Excel TSV pasting[cite: 1].
* **Cartesian Coordinate Plane**: Pure HTML5 Canvas coordinate grid generator designed for classroom handouts, worksheets, and presentations[cite: 1].
  * Configurable domain and range ($X$ and $Y$ min/max/step)[cite: 1].
  * Sub-gridlines (half-step minor gridlines) and selectable grid styles (dashed, dotted, solid)[cite: 1].
  * Axis labels, variable notation ($x$, $y$), origin marker ($O$), and numerical ticks[cite: 1].
  * **Granular Directional Arrowheads**: Master toggle for axis arrows with individual direction toggles:
    * Positive $X$ (Right)
    * Negative $X$ (Left)
    * Positive $Y$ (Top)
    * Negative $Y$ (Bottom)
    * Default state: Enabled with all 4 directions active on reveal.

---

## Styling & Typography

* **Color Palette**: Preset with a curated sequence of 6 grayscale shades, the accessible Okabe-Ito colorblind-safe palette, slate accents, and an arbitrary hex color picker[cite: 1].
* **HTML & Sub/Superscript Parser**: Labels, axis titles, and chart titles support sub/superscript parsing using either standard HTML tags (`<sub>`, `<sup>`) or LaTeX-style shorthand (`x_1`, `x^2`, `H_{2}O`)[cite: 1].
* **Dynamic Contrast**: Data labels and error bars automatically invert their foreground color against dark backgrounds for readability[cite: 1].

---

## Data Input & Import Capabilities

* **Direct Inline Editing**: Dynamic tables allowing rows and columns to be added, reordered, or removed with single-click delete buttons[cite: 1].
* **Spreadsheet Import**: Built-in clipboard parsers allow users to paste tab-separated rows directly from Microsoft Excel or Google Sheets, as well as comma-separated values (CSV)[cite: 1].

---

## Export Utilities

* **Download PNG**: Generates a high-resolution flat PNG image[cite: 1]. For standard charts, the external HTML legend is rendered onto the canvas above the plot before downloading[cite: 1].
* **Copy to Clipboard**: Uses the asynchronous Clipboard API (`image/png` blob) for quick pasting into Word, Google Docs, slides, or emails, with an automated fallback for embedded environments[cite: 1].
* **Copy as HTML Table**: Specifically available when using the Data Table tool to paste semantic HTML markup directly into rich text editors or web pages[cite: 1].

---

## Project Structure

The entire application is encapsulated inside a single distribution file:
