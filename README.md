# Coil-Calculator
To calculate Coil weight if physical weight is not known, as well as knowing lineals with just inner &amp; outer diameter dimension

Estimates coil weight (kg) from dimensions when the actual weight isn't known.
 
**Formula**
 
```
kg = π/4 × (OD² − ID²) × width × density × X factor ÷ 10⁹
```
 
Dimensions in mm, density in kg/m³. The X factor (0–1) allows for gapping between layers: 1.00 is solid metal, 0.95 means 5% of the coil cross-section is air.
 
If profile/thickness is entered, the calculator also shows strip length, weight per metre and approximate number of wraps.
 
## Hosting on GitHub Pages
 
1. Create a new public repository (e.g. `coil-calculator`).
2. Upload `index.html` (and this README) to the repository.
3. Go to **Settings → Pages**, set **Source** to "Deploy from a branch", choose `main` and `/ (root)`, then save.
4. After a minute or so the calculator is live at `https://<your-username>.github.io/coil-calculator/`.
## Embedding
 
Add `?embed=1` to hide the page header and footer, then use an iframe:
 
```html
<iframe src="https://<your-username>.github.io/coil-calculator/?embed=1"
        width="100%" height="760" style="border:0" title="Coil Weight Calculator"></iframe>
```
 
Inputs can be pre-filled from the URL, e.g. `?width=1250&id=508&od=1500&density=7850&factor=0.95&thickness=0.6`.
 
## Changing materials
 
Edit the `MATERIALS` list near the top of the script in `index.html`. Everything is in that one file; there is nothing to build or install.
