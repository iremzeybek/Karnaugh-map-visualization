# LogicLab - Karnaugh Map Visualizer

A Java Swing application that simplifies 4-variable Boolean functions using a Karnaugh map. Built as a CSE 215 project.

## How it works

Pipeline: **Input -> Map -> Groups -> Simplified expression**

- **User interface:** Swing window with a clickable 4x4 grid (Gray code order on both axes), plus Clear, Fill all and Load example buttons.
- **Logic layer:** converts cell values to minterms, finds prime implicants with Quine-McCluskey, then picks a minimal cover (fewest terms, then fewest literals).
- **Validation:** a 16-row truth table compares the original function with the simplified one and shows whether they match.

Each group in the minimal cover is highlighted on the map in its own color.

## Requirements

- Java 8 or newer (JDK)

## Run

```bash
javac LogicLab.java
java LogicLab
```

## Usage

1. Click a cell to toggle it between 0 and 1.
2. The minterm list, simplified expression, groups and truth table update instantly.
3. Use **Load example** to try F = Σm(0, 2, 5, 7, 8, 10).

## Project structure

```
LogicLab.java   # logic layer + Swing UI
```
