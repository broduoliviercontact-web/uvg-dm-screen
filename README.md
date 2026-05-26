# UVG Digital DM Screen

An interactive, browser-based DM screen for **Ultraviolet Grasslands and the Black City**. It gathers travel tools, encounter tables, trade helpers, setting generators, zoa creation tables, and campaign-facing utilities into a single retro terminal interface.

This repository preserves the spirit of the original UVG digital screen by **Saker Tarsos** and adds a maintained static deployment with English and French entry points.

## Live Site

- English: <https://dewy-marvel-wef8.here.now/>
- Français: <https://dewy-marvel-wef8.here.now/fr/>
- Original source page: <https://tarsostheorem.blogspot.com/p/uvg-digital-dm-screen.html>

## What's Inside

| Section | Includes |
| --- | --- |
| DM Tools | Hero generator, UVG skills, NPC voyager, GM power, death oracle |
| Biomagic Corruption | Exposure level and mutation tables |
| Travel | Quests, carousing, misfortune, encounters, chases, discoveries, directions, foraging |
| Setting | History, culture, languages, locations, discoveries, climate, geography |
| Rumors | Cats, Humanity, Porcelain Princes, Spectrum Satraps, Steppe Nomads, Ultras, Vomes |
| Supplies | Essentials, toolkits, vehicles, hirelings, ranged weapons, melee weapons |
| Trade | Market research, haggling, trade goods, route risk, trade obstacles |
| Zoa Generator | Lifeform kingdoms, viruses, bacteria, archaea, protozoa, fungi, animals, golems, daimons |
| Neozoa Modificator | Strange creature modifications and corruptions |
| Research | Expeditions, fake research risks, humorous/mundane/terrifying events |
| Travel Companion | Location-specific UVG encounter, discovery, misfortune, and special tables |

## French Version

The French page lives at [`site/fr/index.html`](site/fr/index.html).

Current French coverage focuses on:

- navigation and control labels
- visible section and table buttons
- short help text for the main toolbox
- trade instructions and key generated result labels
- HTML validity fixes for the French mirror

The long embedded UVG table results are still mostly inherited from the English source. They are intentionally left intact for now so the generators remain stable and faithful to the original tables.

## Project Structure

```text
site/
  index.html       English static app
  fr/index.html    French static app
  index_fr.html    French mirror kept for compatibility
```

Everything is static HTML, CSS, and JavaScript. There is no build step, package manager, backend, or runtime dependency.

## Run Locally

Open the files directly in a browser, or serve the folder locally:

```bash
python3 -m http.server 4173 --directory site
```

Then visit:

- <http://127.0.0.1:4173/>
- <http://127.0.0.1:4173/fr/>

## Deploy

The current public site is hosted on here.now. To update the existing deployment:

```bash
publish.sh site --slug dewy-marvel-wef8
```

The deployed site is static, so publishing the `site/` directory is enough.

## Credits

- **Game**: [Ultraviolet Grasslands and the Black City](https://www.drivethrurpg.com/product/338383/Ultraviolet-Grasslands-and-the-Black-City), by Luka Rejec
- **Original digital screen**: Saker Tarsos, [Tarsos Theorem](https://www.tarsostheorem.com/)
- **Static mirror and French localization work**: this repository

## Fan Work Notice

This is a non-commercial fan tool for table use. Ultraviolet Grasslands and its setting belong to Luka Rejec. Original table text and digital screen work are credited above.
