# WebGPU Shadertoy

![WebGPU](https://img.shields.io/badge/WebGPU-Enabled-brightgreen) ![Tailwind](https://img.shields.io/badge/UI-Tailwind-blue) ![License](https://img.shields.io/badge/License-MIT-green)

---

## Live Demo

[Access the Live Application](https://f0rtin.github.io/WebGPU-3D-Scene/)

Create and manipulate **3D objects** in real-time directly in your browser using **WebGPU** and an **SDF (Signed Distance Field)** based rendering engine.

---

## Overview

This project is an **interactive 3D rendering application** running in the browser, leveraging **WebGPU** for hardware acceleration and **Tailwind CSS** for a responsive user interface. Users can dynamically add and manipulate spheres, cubes, and tori in a 3D scene, which is procedurally rendered using **SDFs** and simple lighting.

Objects can be selected and their properties (**position**, **scale**, **color**) modified in real-time via a sidebar panel. The scene also includes a ground plane with a checkerboard pattern.

---

## Key Features

* **Real-time** interactive 3D rendering with **WebGPU**.
* **Dynamic object addition**: Spheres, Cubes, Tori.
* **Real-time property modification**: Position, Scale, Color.
* **Orbital camera** control using mouse and arrow keys.
* Ground plane with checkerboard pattern and simple lighting.
* Responsive UI with a sidebar panel for objects and properties.
* Real-time **FPS** display.
* Performance limited to **10 simultaneous objects** in the scene.

---

## Shader Implementation

The core rendering logic is handled by the shaders.

### Vertex Shader

* Generates a full-screen triangle to cover the entire canvas, enabling full-screen rendering for raymarching/SDF techniques.

### Fragment Shader

* Uses **Signed Distance Fields (SDFs)** to calculate the minimum distance from the viewpoint to every object in the scene.
* Renders spheres, cubes, and tori based on their type.
* Adds a ground plane with a checkerboard pattern.
* Calculates **simple lighting** (Lambertian) for both objects and the plane.
* Manages the orbital camera based on mouse input.

---

## Getting Started

### Requirements

* A modern browser with **WebGPU support** (Chrome 113+, Edge 113+).
* Internet connection for CDN dependencies (Tailwind, CodeMirror).

### Installation

1. Clone the repository:
    ```bash
    git clone [https://github.com/YOUR_USERNAME/WebGPU_ShaderToy.git](https://github.com/YOUR_USERNAME/WebGPU_ShaderToy.git)
    cd WebGPU_ShaderToy
    ```
2. Open `index.html` in a WebGPU-compatible browser.

> No server installation or local dependencies are required.

### Project Structure

```graphql
WebGPU_ShaderToy/
├── index.html           # Main file with HTML, CSS, and JS
├── README.md
└── assets/              # Optional assets (not included in this code)
```
## Usage

- Launch the application in your browser.
- Add objects to the scene using the buttons: `+ Sphere`, `+ Cube`, `+ Torus`.
- Click on an object to select it.
- Modify its properties in the sidebar panel: Position X/Y/Z, Scale, Color.
- Move the camera with arrow keys.
- Delete an object using the `×` button.

---

## Technical Stack

| Component      | Role                                              |
|----------------|--------------------------------------------------|
| WebGPU         | Hardware acceleration for GPU rendering         |
| HTML5 Canvas   | Rendering surface                                |
| Tailwind CSS   | Responsive UI framework                          |
| CodeMirror     | Integrated code editor (planned for extensions) |
| JavaScript (ES6) | Scene logic, object management, and shader handling |

---

## Performance Metrics

- Real-time rendering with displayed FPS
- Limit of 10 objects to maintain smooth performance
- Compatible with high-resolution displays (DPR support)

---

## ⚠️ Troubleshooting

- **WebGPU Not Supported:** An error message will be displayed. Please use a compatible browser.
- **Low FPS:** Check the number of objects in the scene and the canvas resolution.
- **UI Interactions:** Properties will only update if an object is actively selected.

---

## License

MIT License – See the LICENSE file for more details.

---
