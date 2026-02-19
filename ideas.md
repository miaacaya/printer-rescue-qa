# Printer Help Desk Web App - QA Concept

## Overview
Web app to guide help desk users through printer troubleshooting. Focused on **Canon, Epson, Lexmark, Zebra** for now. Includes model selection, guided flows, and a virtual simulator for printers with screens.

---

## Features to Test

### 1. Brand Selection
- Users can select a printer brand (Canon/Epson/Lexmark/Zebra)
- Edge cases:
  - Selecting a brand that has no models yet
  - Switching brands mid-flow
- Expected behavior:
  - Brand selection leads to correct brand page
  - Switching brands preserves or warns about unsaved progress

### 2. Model Search
- Users type in printer model
- Shows picture of printer and troubleshooting guides:
  - Calibration
  - Network reset
  - Factory reset
- Edge cases:
  - User enters invalid model
  - Partial matches
  - Model not found
- Expected behavior:
  - Display correct image + guides
  - Suggest “unknown model” flow if no match

### 3. Virtual Simulator Mode
- For printers with screens
- Users can press virtual buttons
- Edge cases:
  - Incorrect button presses
  - Users trying sequences not supported
- Expected behavior:
  - Simulator responds as if real printer
  - Shows correct menu navigation

### 4. UI / UX Considerations
- Mobile view (user standing at printer)
- Large search bar is visible and usable
- Clear instructions for each step

---

## Potential Test Cases (Manual)
1. Brand dropdown displays all 4 brands correctly
2. Clicking a brand navigates to correct page
3. Typing a valid model shows image and guides
4. Typing an invalid model triggers “unknown model” flow
5. Simulator buttons work as expected for Canon printer
6. Simulator buttons work as expected for Zebra printer
7. Switching brands mid-flow prompts warning or preserves state
8. Mobile view shows search bar and instructions clearly

---

## Notes / Ideas for Later
- Expand to more brands
- Add copy-to-clipboard ticket summary
- Include print-friendly guide PDFs
- Include screenshots for negative paths for test reporting
