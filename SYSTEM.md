# SYSTEM — Plating as Composition

A plate is a canvas with constraints. It's circular (usually), white (usually), and the chef has arranged elements on it according to a logic that took years to develop. The photography reveals or destroys that logic depending on the angle, the light, and the decisions made in the prompt.

---

## Colour temperature is not a preference — it is the dish

Food is more temperature-sensitive than any other luxury category subject.

| Temperature | Effect on food |
|---|---|
| **2700–3000K** | Maximum appetite appeal — warmth, richness, browning reads as caramelised |
| **3400–3800K** | Editorial warmth — food reads as crafted and warm without looking commercially overlit |
| **4200–4500K** | Neutral — good for raw ingredients, fish, dairy; can make cooked meat look undercooked |
| **5000–5500K** | Nordic cold — fine for vegetables and herbs, harsh on proteins |
| **6000K+** | Clinical. Food looks unappetising in most registers. Correct only for raw seafood and scientific ingredient studies |

Always specify the K value explicitly. Never write "warm light" — specify `3600K diffuse overhead`.

---

## Sauce behaviour

Liquid elements (sauces, consommés, reductions, oils) are the most technically complex part of gastronomy photography. They have:
- Surface tension that creates a meniscus at plate edge
- Depth that reads differently under different light angles
- Specular behaviour that distinguishes a thin jus from a thick emulsion

**Prompting for sauce:**

| Sauce type | Light requirement | Prompt element |
|---|---|---|
| Clear consommé / broth | Backlit or transmitted | `transmitted light through consommé, depth visible, amber internal glow` |
| Dark reduction / jus | Overhead + side | `specular highlight on jus surface, depth in sauce around protein` |
| White emulsion / beurre blanc | Soft overhead | `matte surface on emulsion, no specular — texture without glare` |
| Olive oil drizzle | Raking or overhead | `oil pools visible, slight specular on surface, golden colour` |
| Foam / espuma | Macro overhead | `individual bubble structure visible, translucent walls, soft overhead` |

---

## Negative space management

Michelin plating uses the white plate as compositional space. The ratio of food to plate is typically:

| Register | Food-to-plate ratio | Signal |
|---|---|---|
| Haute cuisine | 30–40% food | Price and restraint |
| Bistronomy | 50–60% food | Value and generosity |
| Brasserie | 70–80% food | Abundance |

The model will fill negative space unless told explicitly not to. Add to every haute cuisine prompt: `wide white plate margin preserved — do not add sauce or elements to empty plate area`.

---

## The garnish problem

AI models add garnishes by default — a sprig of herb here, a flower there. Real garnishes in haute cuisine are specific: they reference an element in the dish, they have geometric intention, and they appear in a deliberate position.

**How to control garnish:**

Bad: `with garnish` — model adds random decorative elements  
Better: `no garnish` — if you want pure composition  
Best: `single micro-herb at 2 o'clock position, no other garnish` — specify position like a clock face

---

## The protein-to-negative-space relationship

In haute cuisine plating, the protein is rarely centred. It sits offset, and the sauce relates to it in a specific geometry. The photography has to show both the protein's position AND its relationship to the sauce.

**Prompt approach:**
```
[PROTEIN] placed at 7 o'clock position on white plate,
[SAUCE] pooled from 5 to 9 o'clock position, avoiding protein,
[GARNISH] at 11 o'clock, [ELEMENT] between protein and garnish,
wide white plate margin, no elements above 12 o'clock
```

Treat the plate like a clock face. It gives the model a spatial instruction it can execute.
