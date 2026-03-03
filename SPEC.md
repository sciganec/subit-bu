# SUBIT‑BU Specification  
Formal specification of the minimal SUBIT‑BU system.

---

## 1. Purpose
SUBIT‑BU is a minimal state‑optimization system based on six sensory modalities and a single XOR‑based transformation. It provides a compact, deterministic method for stabilizing subjective state through one reversible bit‑level operation.

The system defines:
- a 6‑axis sensory input model,
- a 6‑bit state representation (SUBIT‑64),
- a minimal optimization rule,
- a mapping from bit‑change to micro‑action (ACT‑1).

---

## 2. Sensory Modalities
SUBIT‑BU uses six independent, embodied sensory axes. Each axis corresponds to one bit in the SUBIT‑64 state.

| Bit | Axis       | Description |
|-----|------------|-------------|
| b5  | Vector     | Orientation of attention |
| b4  | Rhythm     | Internal tempo or pacing |
| b3  | Structure  | Number of active elements in awareness |
| b2  | Action     | Activation vs. inertia |
| b1  | Tension    | Physiological arousal or compression |
| b0  | Focus      | Width or precision of attention |

Each axis is independent, body‑felt, minimal, and irreducible.

---

## 3. SUBIT‑64 State
The system encodes state as a 6‑bit binary number:

s = b₅ b₄ b₃ b₂ b₁ b₀

where:

s ∈ [0, 63]

The bit order reflects decreasing structural influence:  
higher‑order bits represent coarse‑grained orientation; lower‑order bits represent fine‑grained attentional precision.

---

## 4. Minimal Optimization Rule
SUBIT‑BU performs exactly one optimization step per cycle.

### 4.1. Rule
1. Identify the highest‑order active bit (leftmost ‘1’).  
2. Construct a mask for that bit:  
   m = 2ⁱ  
3. Apply XOR:  
   s′ = s XOR m

### 4.2. Properties
- Only one bit changes.  
- The number of active bits never increases.  
- The transformation is reversible.  
- The system always moves toward a simpler, more stable configuration.

---

## 5. ACT‑1 Mapping
The changed bit determines the corrective micro‑action.

| Bit | Axis       | ACT‑1 Description |
|-----|------------|-------------------|
| b5  | Vector     | Adjust direction of attention |
| b4  | Rhythm     | Adjust internal tempo |
| b3  | Structure  | Remove or simplify one element |
| b2  | Action     | Start or stop a micro‑action |
| b1  | Tension    | Reduce physiological intensity |
| b0  | Focus      | Narrow or stabilize focus |

ACT‑1 is always short, actionable, embodied, and immediately performable.

---

## 6. Algorithm (Pseudocode)

```
function SUBIT_BU(s):
    for bit in [b5, b4, b3, b2, b1, b0]:
        if s has bit = 1:
            m = mask(bit)
            s_new = s XOR m
            act1 = interpret(bit)
            return (s_new, act1)
```

---

## 7. Example

### Input
s = 101011₂ = 43

### Highest active bit
b5

### Mask
m = 100000₂

### Optimization
s′ = 101011 XOR 100000  
s′ = 001011₂  
s′ = 11

### ACT‑1
“Shift your attention to a single direction.”

---

## 8. System Characteristics
- minimal (one‑bit change)  
- deterministic  
- embodied  
- reversible  
- stabilizing  
- isomorphic (6 axes ↔ 6 bits ↔ 1 rule)

---

## 9. Version
SUBIT‑BU v1.0.0  
Minimal State Optimization Engine

---
