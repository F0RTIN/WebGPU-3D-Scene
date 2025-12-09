# WebGPU Shadertoy

![WebGPU](https://img.shields.io/badge/WebGPU-Enabled-brightgreen) ![Tailwind](https://img.shields.io/badge/UI-Tailwind-blue) ![License](https://img.shields.io/badge/License-MIT-green)

---

## 🚀 Live Demo

[Access the Live Application](#)

Create and manipulate **3D objects** in real-time directly in your browser using **WebGPU** and an **SDF (Signed Distance Field)** based rendering engine.

---

## 💡 Overview

This project is an **interactive 3D rendering application** running in the browser, leveraging **WebGPU** for hardware acceleration and **Tailwind CSS** for a responsive user interface. Users can dynamically add and manipulate spheres, cubes, and tori in a 3D scene, which is procedurally rendered using **SDFs** and simple lighting.

Objects can be selected and their properties (**position**, **scale**, **color**) modified in real-time via a sidebar panel. The scene also includes a ground plane with a checkerboard pattern.

---

## ✨ Key Features

* **Real-time** interactive 3D rendering with **WebGPU**.
* **Dynamic object addition**: Spheres, Cubes, Tori.
* **Real-time property modification**: Position, Scale, Color.
* **Orbital camera** control using mouse and arrow keys.
* Ground plane with checkerboard pattern and simple lighting.
* Responsive UI with a sidebar panel for objects and properties.
* Real-time **FPS** display.
* Performance limited to **10 simultaneous objects** in the scene.

---

## 🖥️ Shader Implementation

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

## 🛠️ Getting Started

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
### Usage

1. Lancer l'application dans votre navigateur.
2. Ajouter des objets à la scène à l'aide des boutons : `+ Sphère`, `+ Cube`, `+ Tore`.
3. **Cliquer** sur un objet pour le sélectionner.
4. Modifier ses propriétés dans le panneau latéral : **Position X/Y/Z**, **Échelle**, **Couleur**.
5. Déplacer la caméra avec la **souris** ou les touches fléchées.
6. Supprimer un objet à l'aide du bouton `×`.

---

## ⚙️ Pile Technique (Technical Stack)

| Composant | Rôle |
| :--- | :--- |
| **WebGPU** | Accélération matérielle pour le rendu GPU. |
| **HTML5 Canvas** | Surface de rendu. |
| **Tailwind CSS** | Framework d'interface utilisateur responsive. |
| **CodeMirror** | Éditeur de code intégré (prévu pour extensions). |
| **JavaScript (ES6)** | Logique de la scène, gestion des objets et des shaders. |

---

## 📈 Métriques de Performance (Performance Metrics)

* Rendu en temps réel avec **affichage des FPS**.
* Limite de **10 objets** pour maintenir des performances fluides.
* Compatible avec les écrans haute résolution (prise en charge du **DPR**).

---

## ⚠️ Dépannage (Troubleshooting)

* **WebGPU non supporté** : Un message d'erreur sera affiché. Veuillez utiliser un navigateur compatible.
* **FPS bas** : Vérifiez le nombre d'objets dans la scène et la résolution du canvas.
* **Interactions UI** : Les propriétés ne se mettront à jour que si un objet est **activement sélectionné**.

---

## 📝 Licence (License)

**Licence MIT** – Voir le fichier LICENSE pour plus de détails.

---

## 👤 À Propos (About)

Développé pour démontrer un **moteur de rendu 3D interactif** basé sur les **SDF** dans le navigateur, utilisant **WebGPU** pour l'accélération matérielle et une interface moderne construite avec **Tailwind CSS**.