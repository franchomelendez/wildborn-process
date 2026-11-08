# Wildborn — Game Design Dev Log

## What this repo is
A standalone HTML page (`index.html`) served as a public dev log for "Wildborn", embedded inside the parent Ingimeon/Wildborn site. It documents the game design process step by step.

## Project
- **Game title:** Wildborn
- **Genre:** 2D exploration + combat. Camera not decided: started as a side-scroller, now testing isometric (8-direction sprites)
- **Target audience:** Ages 8–12
- **Visual style:** Anime / manga
- **Status:** Design phase

## Characters
| Name | Animal | Role | Trait |
|------|--------|------|-------|
| Coco | Fox-girl | Protagonist | Curious explorer |
| Charlotte | Panda-girl | Secondary | Loyal fighter |
| Milo | Wolf-boy | Secondary | Fierce & loyal |
| Otto | Bear-boy | Secondary | Gentle giant |
| Juno | Red panda-girl | New | Inventor |

## Story (summary — full version in the page's Story section)
A tribe on a hidden island made a syrup giving animal strength to fight pirates who hid treasure there; a few pirates escaped with some. Years later a doctor found it (museum) and offered it to parents of babies who wouldn't survive birth. The kids became human–animal hybrids, raised in secret at a remote private school. Coco finds the doctor's photo; the trail leads to the island, where the game starts. Open: how the syrup left the island, surviving tribe, the doctor's motive.

## Island locations
8 locations: Sandy Cove (start), The Great Treehouse (home base), The Howling Caves, The Bamboo Maze, The Shadow Lagoon, The Ruined Temple, The Stormy Peaks, The Whispering Grove.

## Assets
Concept art lives in `assets/concept_art/`; all images are referenced with relative paths from `index.html`.

| File | Subject |
|------|---------|
| `Fox-girl explorer character design.png` | Coco — front/side/back + face closeup |
| `Panda-girl character reference sheet.png` | Charlotte — front/side/back + face closeup |
| `Young wolf-boy character design sheet.png` | Milo — front/side/back + face closeup |
| `Bear-boy character design sheet.png` | Otto — front/side/back + face closeup |
| `Tropical island adventure map.png` | Parchment-style illustrated island map |
| `red-panda-front.webp` | Juno — front view cropped from her turnaround |

`assets/profiles/{coco,charlotte,juno}-profile.webp` — profile sheets (traits, expressions, signature line), from `../../Concept Art/* Profile Sheet.png`.

`assets/turnarounds/*-turnaround.webp` — the 5-view isometric sheets (s, sw, w, nw, n), converted from `../../Concept Art/`.

`assets/sprites/*.gif` — walk-cycle previews built from the packed sheets in `../../wildborn-sprites/out/` (25 frames, 40 ms each, on `#f7f5f2`).

## Tech
- Pure HTML + inline `<style>` in `index.html`, no framework, no build step
- Uses CSS custom properties from a parent site theme — never hardcode values that use `var(--...)` tokens
- No JavaScript
- Images referenced with relative paths (spaces in filenames are fine in quoted `src` attributes)

## Design conventions
- Brand colors: forest green `#3B6D11`, amber `#BA7517`, mid-green `#639922`
- Cards: `var(--color-background-primary)` background, `0.5px solid var(--color-border-tertiary)` border
- Section structure: `.section-label` (small caps label) → `.section-title` → `.section-desc` → content
- Devlog: `.log-dot.done` = green checkmark (completed), `.log-dot` with `○` = pending
- Progress bar gradient: `linear-gradient(90deg, #3B6D11, #BA7517)`
