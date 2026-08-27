# higgsfield-gastronomy-prompts

**Gastronomy photography is a conversation between a chef's intention and a photographer's interpretation — and AI content is the first medium that can do both simultaneously.**

Every plate is a composition that someone spent years learning to make. The photography has to show not just what it looks like but what it means — the restraint in the negative space, the precision of the sauce work, the geometry of the garnish. Get it wrong and it looks like food. Get it right and it looks like a restaurant worth three hours of your life and €300.

This repository documents the specific decisions — plating angle, light colour temperature, surface selection, sauce behaviour, negative space management — that make AI gastronomy content indiscernible from editorial food photography shot in a Michelin kitchen.

Built alongside **[higgsfield-luxury-prompts](https://github.com/AlexianIulian/higgsfield-luxury-prompts)** — same methodology, gastronomy application.

---

## Why gastronomy is the hardest editorial category

Every other luxury category photographs an object. Gastronomy photographs a *decision* — the chef's intention crystallised in a specific arrangement that will never exist again in exactly this form.

**Four problems unique to this category:**

| Problem | Why it's hard | Solution |
|---|---|---|
| **Colour temperature** | Food is uniquely sensitive to light temperature — warm light makes it appetising, cold light makes it clinical, wrong temperature makes it unrecognisable | Always specify K, always test at ±200K |
| **Sauce behaviour** | Liquid elements (sauces, consommés, oils) require specific light to show their texture and depth — most prompts render them flat | Specify `specular highlight on sauce surface`, `depth visible in consommé` |
| **Plating geometry** | Chefs compose on a plate as deliberately as a painter on a canvas — the AI must preserve that geometry, not "improve" it | Describe the arrangement explicitly, not vaguely |
| **Negative space** | Fine dining plating uses the white of the plate as part of the composition — the model will fill it | Explicit instruction: `wide negative space on plate, do not fill` |

---

## Register map

| Register | Key references | Angle | Light | Surface |
|---|---|---|---|---|
| **French haute cuisine** | Robuchon · Ducasse · Le Bernardin | 45° | Warm diffuse 3600K | Linen · aged oak |
| **Nordic / new Nordic** | Noma · Geranium · Frantzén | 80° near-overhead | Flat overcast 5200K | Stone · birch · foraged element |
| **Japanese kaiseki** | Kikunoi · Ryugin · Den | Variable by course | Natural window 5000K | Ceramic · lacquer · bamboo |
| **Contemporary bistro** | Frenchie · Septime · Dilia | 45° three-quarter | Ambient warm 3800K | Marble · concrete · linen |
| **Ingredient raw** | René Redzepi ethos · pre-service | Extreme close overhead | Raking natural | Dark slate · unfinished wood |

---

## The plating-angle system

Camera angle in gastronomy carries meaning that no other category has.

| Angle | What it shows | Register |
|---|---|---|
| **Overhead 90°** | Symmetry and geometry of the plate composition | Japanese kaiseki, Nordic flat compositions |
| **80° near-overhead** | Depth visible, volume visible, still shows full plate | Nordic, contemporary French |
| **60°** | Balance of composition and volume — standard editorial | Bistronomy, modern French |
| **45° three-quarter** | Classic food editorial — shows height, texture, garnish drama | Haute cuisine, Michelin editorial |
| **Horizontal / eye-level** | Height as the argument — towers, mousses, stacked elements | Architectural plating, Tom Kerridge register |

---

## Structure

```
higgsfield-gastronomy-prompts/
├── SYSTEM.md              ← plating as composition, colour temperature, sauce behaviour
├── registers/
│   ├── haute-cuisine.md   ← Ducasse · Robuchon · Le Bernardin · 45° · warm
│   ├── new-nordic.md      ← Noma · Geranium · overhead · cold natural light
│   └── ingredient-raw.md  ← mise en place · pre-service · the ingredient truth
├── mise-en-place/
│   ├── knife-work.md      ← precision cuts · prep surface · raking light
│   └── raw-materials.md   ← market produce · ingredient studies
├── lighting/
│   ├── overhead.md        ← diffuse top light · Nordic register
│   ├── raking.md          ← side light · texture · sauce depth
│   └── backlit.md         ← consommé · broth · translucent element
└── reels/
    └── plating-reveal.md  ← the moment of completion · 6–10s · Seedance 2.5
```

---

## Core principle

> Show the chef's intention. The plate is a composition that exists once.

The AI doesn't invent the dish — it reveals it. Every prompt decision should serve the logic of the plating, not impose an external aesthetic on it.

---

## Status

`active` — built alongside a live production studio.

<div align="center">

built by [@AlexianIulian](https://github.com/AlexianIulian)

</div>
