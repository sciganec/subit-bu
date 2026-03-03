# SUBIT‑BU  
A minimal system for stabilizing subjective state through six sensory modalities and a single XOR‑based optimization step.

## Overview
SUBIT‑BU is a compact state‑regulation engine. It transforms a user’s momentary condition into a 6‑bit SUBIT‑64 state, applies one minimal optimization step, and returns a more stable state together with a single micro‑action (ACT‑1).

The system is designed to be:
- minimal  
- deterministic  
- structurally clean  
- embodied and intuitive  
- mathematically reversible  

## Core Components

### Six Sensory Modalities
SUBIT‑BU uses six independent, body‑felt modalities:

1. **Vector** — orientation of attention  
2. **Rhythm** — internal tempo  
3. **Structure** — number of active elements in awareness  
4. **Action** — activation vs. inertia  
5. **Tension** — physiological arousal  
6. **Focus** — width of attention  

These six axes form a complete, minimal basis for describing subjective state.

### SUBIT‑64
The six modalities map directly to a 6‑bit code:

\[
s = b_5 b_4 b_3 b_2 b_1 b_0
\]

This is the SUBIT‑64 state space (0–63).

### Minimal XOR Optimization
SUBIT‑BU performs exactly one optimization step:

1. Identify the highest‑order active bit (the leftmost `1`).  
2. Construct a mask for that bit.  
3. Apply XOR:

\[
s' = s \oplus m
\]

This removes one unit of structural tension and produces a more stable state.

### ACT‑1 (Micro‑Correction)
The changed bit determines the corrective action:

- **b5 (Vector)** → adjust direction of attention  
- **b4 (Rhythm)** → adjust tempo  
- **b3 (Structure)** → simplify by removing one element  
- **b2 (Action)** → start or stop a micro‑action  
- **b1 (Tension)** → reduce intensity  
- **b0 (Focus)** → narrow or stabilize focus  

Each ACT‑1 is short, actionable, and immediately performable.

## Example

### Input state
```
s = 101011₂ = 43
```

### Highest active bit
`b5`

### Mask
```
m = 100000₂
```

### Optimization
```
s' = 101011 XOR 100000
    = 001011₂
    = 11
```

### ACT‑1
“Shift your attention to a single direction.”

## Repository Structure
- `README.md` — system overview  
- `SPEC.md` — formal specification  
- `ENGINE.md` — engine description  
- `UX.md` — interface description  

## License
MIT License

---
