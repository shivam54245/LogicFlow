# LogicFlow

A snappy, modular 2D digital circuit simulator in TypeScript. It features an infinite canvas, four-valued logic resolution, interactive wiring, custom integrated circuit (IC) creation, and in-place hierarchical inspection ("transparent IC" mode).

---

## Features

- **Four-Valued Logic Engine:** Full support for `0` (LOW), `1` (HIGH), `Z` (High-Z / Floating), and `X` (Contention / Bus conflict).
- **Color-Coded Dynamic Wires:**
  - **Black:** 0V (LOW)
  - **Red:** 5V (HIGH)
  - **Ochre / Amber:** Floating (High-Z)
  - **Crimson / Highlight:** Contention error (`X`)
- **Infinite Canvas:** Smooth pan and zoom centered on your cursor with grid-snapping and viewport culling.
- **Component Palette:**
  - Inputs & Timing: Switches, push buttons, clocks.
  - Logic Gates: AND, OR, NOT, NAND, NOR, XOR, and Tri-State Buffers.
  - Outputs: Single-color LEDs, RGB LEDs, 7-Segment Displays.
- **Custom Modular ICs:** Select any circuit section and package it into a reusable chip with custom boundary pins.
- **Transparent IC Mode:** A global toggle that turns chip casings semi-transparent to reveal their internal gates, connections, and live wire states in real time.

---

## Architecture Overview

To keep the simulation fast and maintainable, the codebase is split into three decoupled modules:
