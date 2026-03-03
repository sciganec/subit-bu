# SUBIT‑BU Engine  
Minimal state‑optimization engine based on a single XOR transformation.

---

## 1. Purpose
The SUBIT‑BU engine performs one deterministic optimization step on a 6‑bit SUBIT‑64 state. It identifies the highest‑order active bit, flips it using XOR, and returns the new state together with the corresponding micro‑action (ACT‑1).

The engine is:
- minimal  
- reversible  
- deterministic  
- structurally stabilizing  

---

## 2. Input
A SUBIT‑64 state represented as a 6‑bit binary number:

s = b₅ b₄ b₃ b₂ b₁ b₀  
where s ∈ [0, 63]

Each bit corresponds to one sensory modality:
- b₅ = Vector  
- b₄ = Rhythm  
- b₃ = Structure  
- b₂ = Action  
- b₁ = Tension  
- b₀ = Focus  

---

## 3. Optimization Rule
The engine performs exactly one step:

1. Find the highest‑order bit where bᵢ = 1.  
2. Construct a mask for that bit:  
   m = 2ⁱ  
3. Apply XOR to flip that bit:  
   s′ = s XOR m

This operation removes one unit of structural tension and produces a simpler, more stable state.

---

## 4. Bit Masks
Masks for each bit:

- b₅ → 100000₂  
- b₄ → 010000₂  
- b₃ → 001000₂  
- b₂ → 000100₂  
- b₁ → 000010₂  
- b₀ → 000001₂  

---

## 5. ACT‑1 Mapping
The changed bit determines the corrective micro‑action:

- b₅ → adjust direction of attention  
- b₄ → adjust internal tempo  
- b₃ → simplify by removing one element  
- b₂ → start or stop a micro‑action  
- b₁ → reduce physiological tension  
- b₀ → narrow or stabilize focus  

---

## 6. Pseudocode

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
b₅

### Mask
m = 100000₂

### Optimization
s′ = 101011 XOR 100000  
s′ = 001011₂  
s′ = 11

### ACT‑1
“Shift your attention to a single direction.”

---

## 8. Engine Characteristics
- **Minimal**: only one bit changes.  
- **Deterministic**: same input → same output.  
- **Reversible**: XOR preserves invertibility.  
- **Stabilizing**: always reduces the number of active bits.  
- **Isomorphic**: directly maps sensory axes to bit structure.  

---

## 9. Version
SUBIT‑BU Engine v1.0.0  
Minimal XOR‑based State Optimization Engine

---
