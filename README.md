# The Blueprint of Us

A romantic, minimalist, and interactive web experience designed to map out a future apartment. Users can click on various rooms to illuminate the space and reveal personal memories and stories associated with each area.

## Features

* **Interactive Blueprint:** Clickable hotspots mapped perfectly to an apartment floorplan.
* **Elegant & Romantic UI:** Clean, minimalist design featuring soft color palettes, gentle hover effects, and beautiful typography (*Cormorant Garamond* and *Montserrat*).
* **Smooth Animations:** Fluid transitions for unlocking the colored layers of the rooms and elegantly centering memory cards on the screen.
* **Responsive Mapping:** A custom "engine" that automatically calculates exact percentage-based mapping from hardcoded pixel coordinates, ensuring the clickable hotspots remain completely accurate regardless of screen size and image scaling.

## Required Files

To run this project correctly, make sure you possess all three of the following files in the primary directory:

* `index.html`: The core application file containing all the HTML structure, CSS styling, and JavaScript logic.
* `blueprint.png`: The base, original image of the apartment layout.
* `colorPrint.png`: The fully colored/illuminated version of the apartment layout (used to gradually reveal colors).

## How to Run

1. Ensure the required image files (`blueprint.png` and `colorPrint.png`) are located in the exact same folder as `index.html`.
2. Open `index.html` directly in any modern web browser (e.g., Chrome, Safari, Firefox). No server setup is required.
3. Click on the different rooms (The Kitchen Island, The Living Area, The Bedroom Sanctuary, etc.) to reveal the colored print and the associated memory! 

## Technical Details

The application works by loading the base image and reading its intrinsic pixel dimensions. A JavaScript engine then parses a dictionary of room coordinates (represented as `[left, top, right, bottom]` pixels) and converts them into precise CSS boundary percentage properties (`clip-path` and positional bounds). 

This approach allows a hidden layer (`colorPrint.png`) to be perfectly masked and revealed seamlessly section-by-section without needing multiple separate image cuts for every room.
