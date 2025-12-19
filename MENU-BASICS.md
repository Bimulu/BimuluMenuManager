# Menu Basics

Alle menuer defineres i YAML-filer under:

## Grundstruktur
```yml
id: main
title: "<gold>Menu</gold>"
rows: 3
items: {}yml```

---

## 🧱 Items
**Side-navn:** `Items`

```md
# Items

Items defineres pr. slot (0–53).

```yml
"13":
  material: DIAMOND
  name: "<aqua>Butik</aqua>"
  lore:
    - "<gray>Klik her</gray>"

---

## 🖱️ Kliktyper & Actions
**Side-navn:** `ClickTypes-and-Actions`

```md
# Kliktyper & Actions

## Kliktyper
- LEFT
- RIGHT
- SHIFT_LEFT
- SHIFT_RIGHT
- MIDDLE
- ANY (fallback)

```yml
actions:
  LEFT:
    run:
      - "OPEN:shop"
---

## ⏱️ Cooldowns
**Side-navn:** `Cooldowns`

```md
# Cooldowns

Cooldowns kan sættes pr. item og kliktype.

```yml
cooldown: "5s"
cooldown_fail:
  - "MESSAGE:Vent %cooldown_remaining%"

---

## ✅ Conditions
**Side-navn:** `Conditions`

```md
# Conditions

Conditions styrer, om actions må køres.

```yml
conditions:
  all:
    - "PERMISSION:vip"
    - "LEVEL_AT_LEAST:10"
