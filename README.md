# Amine–Lignocellulose Interaction Atlas

Interactive web atlas of amine–lignocellulose interactions and reaction pathways computed with DFT and semiempirical xTB (ORCA, implicit water): interaction complexes, proton-transfer paths, a reaction network, and nudged-elastic-band (NEB) minimum-energy paths for nucleophilic reactions of six amines (EA, DEA, TEA, DMA, DMEA, DMBA).

**Live viewer:** enable GitHub Pages (Settings → Pages → Deploy from branch → `main` / root); the atlas is then served from `index.html`.
**Archive:** DOI assigned by Zenodo on release (see `CITATION.cff`).

## Contents
| File | Purpose |
|---|---|
| `index.html` | Shell: Overview, Interaction Atlas, Proton Transfer, Reaction Network, Nucleophilic Reactions tabs |
| `atlas.html`, `library.json` | Interaction Atlas (docking, CCSD(T) ΔE) |
| `proton.html`, `reactions.json` | Proton-transfer paths |
| `nucleophilic.html` | NEB paths and 3D viewer (data embedded in the page) |
| `overview.json`, `network.json` | Overview medians and reaction-network barriers |

## Level of theory and status
This release is the **xTB build (v16)**: xTB NEB-TS in ORCA 6 (`!XTB ALPB(Water) NEB-TS`), barriers from refined saddle points. Jobs flagged *provisional* in the viewer have unresolved issues and are excluded from the Overview medians. B3LYP-D3BJ/def2-SVP (CPCM water) results are being added in a later release.

## Running locally
Browsers block `fetch` on `file://`, so serve the folder:
```
python3 -m http.server 8000
```
and open http://localhost:8000. 3D views load 3Dmol.js from cdnjs and fonts from Google Fonts (internet required).

## License
Data and page content: CC BY 4.0. Code (HTML/JS): MIT. See `LICENSE`.

## Citation
See `CITATION.cff` / `.zenodo.json`.
