# DCIM: Data Centre Impact Model

A toolkit for UK communities facing a proposed data centre. Built for the Oxford Edge Hackathon, November 2026.

**Live site:** https://54gcdk2b5m-boop.github.io/DCIM/

## What's in it

| Page | For | What it does |
|---|---|---|
| [Understand](index.html) | Everyone | How big data centres are (a campus drawn to scale on a satellite map around Buckingham Palace), the four kinds of impact (economic, resource extraction, environmental, cultural), the variables that drive them, and a scrolling story through real UK projects. |
| [For residents](residents.html) | Households | A scenario calculator: generator noise at your home, bills, house prices, jobs, water, carbon in everyday terms, a culture and heritage check with a free-text box, and questions to ask at the planning meeting. |
| [For councils](levy.html) | Councils and parish bodies | A levy calculator with three ways to set the rate, the working shown step by step, a "good deal" checklist, a draft letter, and an explorer of which choices move which impacts. |
| [How it's calculated](methods.html) | Anyone checking the numbers | Every step of the levy calculation, with formulas, a live worked example, confidence marks and sources. |

Every page is a single static HTML file. Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

## How sure are the numbers?

Each figure carries a confidence mark:

- **●●● measured:** a published or official figure (carbon values, benchmark levies, community fund rates).
- **●●○ estimate:** our arithmetic on good UK data (electricity, carbon by grid region, land per MW).
- **●○○ rough:** an assumption or borrowed US evidence (bills, house prices, jobs, the cultural score, the deal checklist).

Known gaps: grid carbon is an average, not the marginal (usually gas) power a new load pulls in; embodied carbon and power-station water are not counted; developers quote MW in different ways.

## Data and sources

- **Grid carbon:** National Energy System Operator, Carbon Intensity API, 12-month regional means, Nov 2025 to Nov 2026. [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
- **UK projects:** UK Data Centre Tracker by AI Energy Intelligence (public pages). No licence is stated; project names, places and capacities are used for non-commercial research.
- **Permanent jobs for 20 UK schemes:** Verdant, *The Jobs Mirage of Data Centres* (2026), annex compiled from council and developer sources.
- **Carbon values, levy benchmarks, community funds:** UK government (DESNZ, Defra), Open Government Licence.
- **UK data centre sites:** ATLAS Global Data Center Map, © Ringmast4r.
- Full list with every row's source: the hackathon dataset `data-centre-impacts.xlsx`.

## Image credit

Satellite map: [Sentinel-2 cloudless 2024](https://s2maps.eu) by EOX IT Services GmbH (contains modified Copernicus Sentinel data 2024), licensed [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/). The tiles are stitched into one image (`palace-satellite.jpg`), which is shared under the same licence. The data centre campus is drawn over it in the browser; its layout is illustrative.

## Not advice

The estimates are prompts for questions, not planning or legal advice.
