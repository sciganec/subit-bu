# SUBIT‑BU UX  
Interface description for the minimal SUBIT‑BU system.

---

## 1. Overview
The SUBIT‑BU interface is designed to be minimal, fast, and fully embodied. Each cycle consists of four screens:

1. Sensory Input (six sliders)  
2. State Display (SUBIT‑64)  
3. ACT‑1 (one micro‑correction)  
4. Dynamics (history of states)

Each cycle is intended to take less than 20 seconds.

---

## 2. Screen 1: Sensory Input
The user interacts with six independent sliders. Each slider corresponds to one sensory modality:

- Vector  
- Rhythm  
- Structure  
- Action  
- Tension  
- Focus  

The user adjusts each slider based on immediate bodily sensation.  
No text explanations, labels, or cognitive descriptions are required.  
The system converts the six slider values into a 6‑bit state:

s = b₅ b₄ b₃ b₂ b₁ b₀

This state is passed to the optimization engine.

---

## 3. Screen 2: State Display
The system displays:

- the current SUBIT‑64 state (0–63)  
- the binary representation (b₅ b₄ b₃ b₂ b₁ b₀)  
- the dominant axis (the highest‑order active bit)  

A single button is shown:

“Correction”

Pressing it triggers the minimal XOR optimization step.

---

## 4. Screen 3: ACT‑1
After optimization, the system presents:

- the new state s′  
- the bit that changed  
- one micro‑action (ACT‑1) derived from that bit  

ACT‑1 examples:

- Vector (b₅): “Shift attention toward one direction.”  
- Rhythm (b₄): “Slow the internal tempo slightly.”  
- Structure (b₃): “Remove one element from awareness.”  
- Action (b₂): “Pause movement for a moment.”  
- Tension (b₁): “Release a small amount of muscular pressure.”  
- Focus (b₀): “Narrow attention to a single point.”  

A single button is shown:

“Done”

The user performs the action and continues.

---

## 5. Screen 4: Dynamics
The system displays a simple history of recent states:

- previous SUBIT‑64 values  
- transitions (s → s′)  
- repeated patterns  
- dominant axes over time  

This screen provides a sense of trajectory without analysis or interpretation.

A single button is shown:

“New Scan”

This returns the user to Screen 1.

---

## 6. UX Principles
The SUBIT‑BU interface follows six principles:

- **Minimality**: only essential elements are shown.  
- **Embodiment**: all input is based on bodily sensation.  
- **Determinism**: one action per cycle, no branching.  
- **Speed**: each cycle is short and repeatable.  
- **Clarity**: no psychological terminology.  
- **Reversibility**: the system never traps the user in a state.

---

## 7. Version
SUBIT‑BU UX v1.0.0  
Minimal Sensory‑Driven Interaction Model

---
