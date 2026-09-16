# Project Documentation: A Humble Plotter (v1.7.2)

## 📌 Project Overview
**A Humble Plotter** is a standalone, single-file HTML/JS/CSS client-side web application built for educators, students, and scientists to generate publication- and quiz-ready graphs, coordinate planes, and data tables[cite: 1].

* **Tech Stack:** Vanilla JavaScript (`'use strict'`), HTML5, CSS3, Chart.js (v4.4.1 UMD), Tabler Icons (v3.31.0 webfont)[cite: 1].
* **Environment:** Standalone browser runtime, iframe-embeddable (e.g., Google Sites), and printable/exportable[cite: 1].
* **Typography:** Arial across UI and canvas; defaults to 12pt axis labels and 10pt ticks. Data tables default to Arial Narrow[cite: 1].

---

## 🎨 Default Grayscale & Tone Scheme (v1.7.2+)
The default plotting colors follow a clean, accessible light-to-dark progression:
1. **Series 1:** `#6b7280` (Mid Gray) | Solid line | Circle marker | Solid fill[cite: 1]
2. **Series 2:** `#d1d5db` (Light Gray) | Dashed (`8 4`) | Square marker | Solid fill[cite: 1]
3. **Series 3:** `#374151` (Charcoal) | Dotted (`2 3`) | Triangle marker | Solid fill[cite: 1]
4. **Series 4:** `#e5e7eb` (Ghost Gray) | Dash-Dot (`8 3 2 3`) | Diamond marker | Solid fill[cite: 1]
5. **Series 5:** `#111827` (Solid Black) | Long Dash (`12 6`) | Cross marker | Solid fill[cite: 1]

---

## 🚀 Key Architectural Features & Recent Updates (v1.7.2)
* **Smart Contrast Error Bars:** Built-in two-pass error bar rendering via `errPlugin` uses HTML5 Canvas clipping (`ctx.clip()`) and WCAG relative luminance (`contrastColor()`). Error bar sections overlapping dark bars automatically render in crisp white while extensions remain solid black.
* **Marker Boundary Protection:** Line graphs, scatter plots, and trendlines set `clip: false` alongside a 6px layout padding configuration, ensuring markers positioned along outer grid boundaries (such as a Y-axis limit of 20) are never clipped or sliced off.
* **Rich-Text Live Formatting:** Interactive `contenteditable` fields support inline Subscript (`Sub`) and Superscript (`Sup`) tags for chart titles, axis labels, group names, and series headers[cite: 1].
* **Canvas Texture & Legend Syncing:** Canvas fill patterns accurately replicate custom bar textures (Diagonal stripes, Crosshatch, Sparse dots, Tint) and line styles across both live previews and downloaded/copied image exports[cite: 1].

---

## 📊 Supported Chart & Tool Types
1. **Bar Graph:** Multi-group comparison (up to 5 groups) with dynamic error bars ($\pm$), wrapped category labels, and smart contrast data labels[cite: 1].
2. **Line Graph:** Multi-series trend analysis with custom SVG markers, distinct stroke patterns, and an integrated second Y-axis (Y2) toggle[cite: 1].
3. **Scatter Plot:** Numeric X/Y correlation mapping with dual-axis error bars and optional linear regression trendlines[cite: 1].
4. **Pie Chart:** Proportional breakdown with outside leader lines for narrow wedges and auto-calculated contrast text[cite: 1].
5. **Histogram:** Frequency distribution with automatic bin calculation or custom start/bin size configurations[cite: 1].
6. **Box & Whisker:** Tukey $1.5 \times \text{IQR}$ distribution spread summaries with outlier handling[cite: 1].
7. **Data Table Tool:** Spreadsheet-style inline editor with live cell styling, column alignments, and dual PNG/HTML table clipboard copying[cite: 1].
8. **Cartesian Plane:** Blank coordinate grid generator with custom numeric ranges, minor/major gridlines, and mathematical origin labeling (`O`)[cite: 1].