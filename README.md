# Image-to-POP Visualizer

> A TouchDesigner project that transforms image input into dynamic visual outputs.

## Overview

Image-to-POP Visualizer rebuilds a still image as animated 3D geometry, generated live inside
TouchDesigner. Each pixel of the source image drives a field of points and threads: brightness
sets depth and color sets light, so the subject is reconstructed from data rather than simply
displayed.

The included example uses a photo of pink peonies (`peony.jpeg`). Over a short loop the
flowers move between a solid, almost photographic form and a soft tangle of threads, all
rendered in real time on the GPU. Swapping the source image reshapes the entire result.

## Demo

▶ **[Watch the demo (demo.mp4)](demo.mp4)**

The clip shows the project running live in TouchDesigner: the peony bouquet rebuilt as woven
geometry on black, dissolving into fine threads and reforming as the animation loops.

## Features

- Image-driven geometry (shape, depth, and color from a single image)
- Seamless looping animation
- Clean compositing with transparent background
- Adjustable motion (noise, speed, displacement)
- Swappable input image

## How it Works

- The image (`peony.jpeg`) is loaded into TouchDesigner  
- Image data is converted into point-based geometry  
- Position, color, and depth are influenced by pixel values  
- Noise and animation operators add motion  

## Setup

**Install**

1. Download and install TouchDesigner from [derivative.ca](https://derivative.ca/download).
2. Download this repository, keeping `NewProject.toe` and `peony.jpeg` in the same folder.

## Usage

1. Open `NewProject.toe` in TouchDesigner. Start playback if needed.
2. Adjust the `speed`, `noise`, `fit`, and `constant` operators to change the motion.
3. To use your own image, replace `peony.jpeg` or point the Movie File In TOP to a new file. A
   subject on a plain black background works best.

## Project Structure

```
.
├── NewProject.toe    # TouchDesigner project
├── peony.jpeg        # Source image
├── demo.mp4          # Demo recording
├── LICENSE           # MIT License
└── README.md
```

## Credits

- Based on a TouchDesigner tutorial by **[PPPANIK](https://youtu.be/GJMIXo8pwSY)** on YouTube.
- Built with **[TouchDesigner](https://derivative.ca/)** by Derivative.

## License

Released under the MIT License. See [LICENSE](LICENSE) for details.
