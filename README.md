
# Rubik's Cube Solver 🧩

A simple web-based **Rubik's Cube Solver** built in **JavaScript** using object-oriented programming. This project demonstrates cube simulation, manual face rotations, random scramble generation, and solving the cube using a basic algorithm. The visual representation is handled using SVG.

---

## ✅ Features

### ✅ Object-Oriented Cube Representation

* Implemented via the `RubiksCube` class.
* Each cube face (`F`, `B`, `R`, `L`, `U`, `D`) stores 9 color values.

### ✅ Manual Rotation Controls

* 12 buttons for clockwise (`F`, `R`, etc.) and counter-clockwise (`F'`, `R'`, etc.) moves.
* Buttons trigger the `rotateFace()` method using cube notation.

### ✅ Cube Scramble

* `generateScrambledCube()` scrambles the cube with 20 random moves.
* Scrambled state is stored in `originalScramble` for potential reverse solving.

### ✅ Solving Algorithm

* Solves any cube using:

  * **Breadth-First Search** (limited depth).
  * **Fallback Reverse Scramble** if needed.
* Solution steps are visually displayed and animated.
* The solution **doesn't need to be optimal**, just valid.

### ✅ Visual Representation

* `getCubeSvg(state)` renders the cube using SVG based on its current state.
* Visual updates occur after every move or solve step.

---

## 💻 How to Run

1. **Open** `rubiks-cube.html` in any web browser.
2. Use the UI buttons to:

   * Scramble the cube.
   * Solve the cube.
   * Reset to the solved state.
   * Manually rotate cube faces.

---

## 🧠 File Breakdown

### `RubiksCube` class

* Stores and manages cube state.
* Methods:

  * `reset()`: Resets cube to solved state.
  * `scramble()`: Generates a random sequence of moves.
  * `move(notation)`: Applies a move.
  * `rotateFaceClockwise()` / `rotateFaceCounterClockwise()`: Rotates a face.
  * `isSolved()`: Checks if the cube is in a solved state.
  * `getStateString()`: Returns cube state as a color string for rendering.

### `CubeSolver` class

* Contains cube-solving logic.
* Uses BFS and fallback algorithms.
* Methods:

  * `solve()`: Attempts to solve using BFS.
  * `reverseScrambleSolve()`: Fallback random strategy using beginner patterns.
  * `executeSequence()`: Applies a move sequence.
  * `reverseMove(move)`: Reverses a move notation.

---

## 📸 Demo Screenshots (Add Manually)

* Solved Cube
* Scrambled Cube
* Solving Animation
* Manual Rotations

---

## ⚠️ Notes

* The goal is to **demonstrate problem-solving** and not provide a full Rubik’s cube simulator.
* The algorithm prioritizes **working logic over optimization**.
* UI and UX are basic but functional.

---

## 📅 To-Do / Future Enhancements

* Add move history and undo/redo.
* Improve solve algorithm for fewer moves.
* Add 3D visualization using WebGL or Three.js.

---

## 👤 Developed By

**Rahul Mehta**
*JavaScript - Rubik’s Cube Challenge*

---
