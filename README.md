# Dong Hyeon Park — Academic Website

A no-build academic portfolio for professor contact and Fall 2027 Ph.D. applications.

The current site is already populated with research, publications/presentations, selected recognition, technical skills, email, and a local copy of the CV.

## Deploy to GitHub Pages

1. Create a GitHub repository named `YOUR_GITHUB_USERNAME.github.io`.
2. Upload **the contents of this folder** to the repository root.
3. In GitHub, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select `main` and `/ (root)`.
6. Open `https://YOUR_GITHUB_USERNAME.github.io/`.

No npm, Jekyll, Python, or build step is required.

## Things to change before sending the URL to professors

### Required

- Replace `YOUR_GITHUB_USERNAME` in the `og:url` line in `index.html`.
- Add a real profile photo.
- Replace the three placeholder research illustrations with your actual research figures/photos.
- Proofread research descriptions against the latest manuscript/CV before publishing.

### Strongly recommended

- Add your personal Google Scholar link once available.
- Add GitHub only if the repositories are polished and relevant.
- Add direct PDF/poster links when you are comfortable sharing them publicly.
- Keep the homepage focused on the research direction you want to pursue in the Ph.D.; remove less relevant items if necessary.

## Profile photo

Save a photo as:

`assets/img/profile.jpg`

Then replace:

```html
<div class="avatar" role="img" aria-label="Profile photo placeholder for Dong Hyeon Park">
  <span>DP</span>
</div>
```

with:

```html
<div class="avatar avatar-photo">
  <img src="assets/img/profile.jpg" alt="Portrait of Dong Hyeon Park" />
</div>
```

and add this CSS:

```css
.avatar-photo img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
```

## Research figures

Current files are conceptual placeholders:

- `assets/img/research-1.svg` — stiffness-tunable stage
- `assets/img/research-2.svg` — PMLSM modeling / force-ripple work
- `assets/img/research-3.svg` — 3-DOF actuator work

Replacing these with your real figures will create the largest improvement in credibility.

Recommended image types:

1. **AlNiCo XY stage:** clean stage photo or stiffness/resonance concept figure + one energy result.
2. **PMLSM:** motor schematic or force-ripple decomposition plot.
3. **Hybrid reluctance actuator:** actuator CAD/photo showing x-y-theta motion.

Avoid full manuscript screenshots with tiny labels.

## CV

The site links to:

`assets/CV_DongHyeonPark.pdf`

Replace that file with a newer CV while keeping the same filename to update the site without changing HTML.

## File structure

```text
.
├── index.html
├── README.md
├── .nojekyll
└── assets
    ├── CV_DongHyeonPark.pdf
    ├── css
    │   └── style.css
    ├── js
    │   └── main.js
    └── img
        ├── favicon.svg
        ├── research-1.svg
        ├── research-2.svg
        └── research-3.svg
```

## Design intent

The page is intentionally a research portfolio rather than a web version of the full CV. The viewing path is:

**Identity / research direction → strongest result → featured research → outputs → recognition → contact / CV**

That is the path a professor can scan quickly from a contact email.
