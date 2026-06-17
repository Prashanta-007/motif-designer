# Grid-Based Motif Designer

## Project Overview

Grid-Based Motif Designer is a web-based application that allows users to create, edit, save, and share motif designs using a 16 × 16 grid canvas.

The application provides tools for designing patterns, selecting colors, loading preset motifs, estimating prices, saving designs, and generating handover documents for production teams.

---

# Features

## 1. Grid-Based Motif Editor

* 16 × 16 grid canvas
* Click cells to color them
* Drag to create patterns
* Real-time canvas updates
* Eraser tool
* Clear canvas option

## 2. Color Selection and Editing Tools

Available colors:

* Black
* Red
* Blue
* Green
* Yellow

Tools:

* Draw tool
* Eraser tool
* Clear canvas

The active color and tool are visible while designing.

---

## 3. Home Screen Navigation

The application contains a home screen with:

* Create New Design
* Saved Designs
* Motif Library

Navigation allows users to move between different sections of the application.

---

# Price Estimation Logic

The application provides a live price estimate while designing.

The pricing formula used is:

```
Final Price =
Base Price + Color Charge + Complexity Charge + Size Charge
```

## Formula Implementation

```
Base Price = 50

Color Charge =
Number of colors used × 20

Complexity Charge =
Number of filled grid cells × 2

Size Charge =
Grid dimensions × 1
```

## Explanation

* More colors used in the motif increase the price.
* A denser pattern increases the complexity cost.
* Larger motif dimensions increase the final price.

The price updates automatically whenever the user draws, erases, or changes the design.

---

# Grid Canvas Data Structure

The motif canvas uses a 16 × 16 grid.

Total cells:

```
16 × 16 = 256 cells
```

Each grid cell is represented as an HTML element.

The design is stored as an array containing the color value of each cell.

Example:

```
[
"red",
"blue",
"white",
"green"
]
```

Each array position represents one grid location.

Example:

```
Index 0   → First cell
Index 1   → Second cell
Index 255 → Last cell
```

This structure is used for:

* Drawing patterns
* Editing designs
* Saving designs
* Loading designs
* Exporting designs

---

# Motif Library

The application includes preset motifs:

* Flower motif
* Diamond motif
* Border motif

Users can:

* View preset motifs
* Load a motif onto the grid
* Edit the loaded design
* Save the modified version

---

# Saved Designs

The application allows users to manage previous designs.

Features:

* Save current design locally
* View saved designs
* Reopen saved designs
* Duplicate designs
* Delete designs

Saved designs are stored using browser local storage.

---

# Order Handover PDF

The application can generate a production handover summary.

The PDF contains:

* Design name / Order ID
* Pattern dimensions
* Colors used
* Complexity information
* Estimated price
* User notes

The PDF can be downloaded and shared with the production team.

---

# Sharing and Export

Users can export:

## Design Image

The motif can be exported as an image file.

## Design Data

The grid information can be exported as JSON data.

## Handover Summary

The design summary can be exported as a PDF document.

---

# Setup Instructions

## Requirements

* Web browser (Firefox / Chrome)
* Linux, Windows, or Mac system

## Running the Application

1. Download or clone the repository.

2. Open the project folder.

3. Open:

```
index.html
```

in a browser.

OR run from terminal:

```
firefox index.html
```

The application will start in the browser.

---

# Technologies Used

* HTML
* CSS
* JavaScript
* Browser LocalStorage
* jsPDF Library

---

# Project Structure

```
Motif-Designer/

│
├── index.html
│
└── README.md
```

---

# Author

Prashanta Rajon Barooah
