# A4 Label Generator

**▶ Use it online: https://mayoogh-flexli.github.io/a4-label-generator/** — nothing to install. It works in
Chrome or Edge, and nothing leaves your computer.

A single-file tool for making custom-size labels that print on A4 paper. Open `index.html` in Chrome or
Edge. It needs no install and works offline.

## Use

**Several label sizes on one sheet.** The *Label sizes on this sheet* list at the top works like tabs:
- Click **+ Add size** to add size B, C and so on.
- Click a size to edit its text, width × height, font size and colours.
- The sheet fills row by row: all of A, then B starting on a new row, then C, and onto new pages as needed.
- ▲ / ▼ changes the order on the sheet, and ✕ removes a size.
- Every row boundary is a straight full-width cut; after that, cut each strip into its labels.
- Font, border, gap, margin, cut lines and ruler apply to all sizes.

1. **Label text.** *Type a list* is the default. Pick one:
   - **Numbered:** enter prefixes separated by commas (e.g. `R01-C1, R01-C2`) and a start–end range.
     This gives `R01-C1-01 … R01-C1-20`, then `R01-C2-01 …`.
   - **Type a list:** enter one label per line.
2. **Label size.** Enter the width (X) and height (Y) in mm. The tool works out how many labels fit on the
   A4 sheet, centres the grid, and adds more sheets when needed.
3. **Appearance:**
   - **Border thickness** in mm (0 means no border).
   - **Corner radius.**
   - **Label colour** and **text & border colour.** There are also quick presets: white, black, yellow,
     red, blue, green and orange.
   - **Dotted cutting lines** run through the middle of each gap, or along the label edge when the gap is 0.
   - **Ruler scale** along the top and left edges of the sheet (mm from the paper edge). Measure between
     two numbers on a printed sheet to confirm it printed at 100%. While the ruler is on, the page margin
     is at least 12 mm, so labels never cover it.
   - **Font:** Bahnschrift Condensed only. It's compact and easy to read, and ships with Windows 10/11. **Bold** is on by default.
4. **Output:**
   - **Save as PDF** downloads a vector A4 PDF straight away, for example
     `labels_R01-C1-01_40pcs_40x12mm.pdf`.
   - **Print** opens the browser print dialog. Print at **100% / Actual size**, with "Fit to page" turned
     off. If the colours are missing, tick "Background graphics".

**Preview:**
- **Ctrl + mouse wheel** over the sheet zooms in and out around the cursor. The plain wheel scrolls.
- **Click and drag** the sheet to move around it.
- **−**, **+** and **Reset** are in the toolbar; Reset fits the sheet to the window width.

*Shrink text to fit* reduces the font size on small labels so the text stays inside the label.
*Skip first* leaves the first N places empty, so you can reuse a partly cut sheet.

## Project files (editable)

**📄 New** starts an empty project (using your saved default sizes and style). **💾 Save** saves everything to a `.labels.json` file: every size, its text, colours and all the
settings. **📂 Open** loads it back so you can keep editing. Keep one file per robot or panel
(e.g. `R01-motherboard.labels.json`) and reopen it whenever something changes. The PDF is just for printing.

- **Chrome/Edge:** the first save asks where to put the file. After that, **Save** or **Ctrl+S**
  updates the same file.
  - **Save as new file**, or **Ctrl+Shift+S**, makes a copy.
  - **Ctrl+O** opens a project.
- **Other browsers:** each save downloads a new copy.
- The line under the buttons shows the open project's name and whether it has **unsaved changes**.

## Settings

- The tool remembers your last settings automatically.
- **Save as default** stores the current settings. **Reset to default** returns to them.
- **Restore factory settings**, a link under those buttons, forgets your saved default.
- Settings are stored in the browser on this PC, so a different PC or browser starts with the factory
  settings.

How the PDF draws text: each label's text is drawn in Bahnschrift Condensed at 1200 dpi and embedded as a sharp
black-and-white image in the text colour, so the PDF matches the preview. Labels, borders, cut lines and the ruler are vector.