# SVM Explorer

An interactive WebXR mixed reality educational app built with [XR Blocks](https://xrblocks.github.io/) and Three.js that intuitively teaches the fundamentals of Support Vector Machines (SVMs) through hands-on 3D exploration.

**Try it**: https://saeedha-n.github.io/svm-explorer/

## Features

- **Mixed Reality Workspace:** Renders a $0.6\text{ m}$ wireframe data box alongside movable spatial UI panels (*Controls* and *Lesson*) over passthrough.
- **4 Interactive Lessons:**
  1. **Separate Two Groups:** Explore linearly separable 3D clusters from any angle.
  2. **Maximize the Margin:** Tilt, turn, and slide the decision boundary by hand or slider to see live gap width and misclassified point counts, or animate to the optimal SVM boundary.
  3. **Support Vectors:** Drag individual data points in real time and watch the SVM solver recalculate the boundary only when support vectors move.
  4. **The Kernel Trick:** Lift non-separable concentric ring data into a third dimension ($y \propto r^2$, where height $y$ is proportional to $r^2$, the squared distance from the center) so a flat hyperplane can cleanly divide the classes.
- **Zero External ML Libraries:** Includes a custom sub-gradient descent linear SVM solver written in plain JavaScript.

## Running it

| Device | How |
| --- | --- |
| Meta Quest | Open the link in the Meta Quest Browser and press **Enter XR** |
| Android XR | Open the link in Chrome and press **Enter XR** |
| Desktop | Open the link in Chrome to use the built-in simulator with a mouse |

To run locally, serve the folder using with any local static web server (required for ES modules and WebXR) (e.g., `npx serve .` or `python -m http.server`) and open it in Chrome.

The whole app is a single `index.html` file with no build step.