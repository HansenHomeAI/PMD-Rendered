# PMD Rendering Revised Local Mirror

This workspace now contains a local mirror of the viewer and its repo-local dependencies:

- `indexes/index(PMD-Rendering-Revised).html`
- `shared/obj-home-editor.mjs`
- `assets/Terrain-Fixed-Comp.glb`
- `assets/Buildings-Fixed-Comp.glb`
- `assets/Cutout-optimized.glb`

## What is local now

- The HTML file is local.
- The home-model editor module is local.
- The two configured GLB scene assets are local.
- The cutout GLB is local and available for the editor/export flow.

## What is still external at runtime

- Google Fonts
- `unpkg.com` for `three` and `@lumaai/luma-web`
- `lumalabs.ai` for the PMD splat source
- `raw.githubusercontent.com` for UI icons
- `gstatic.com` for Draco decoders used by the GLB loader

## Local server

Run from this directory:

```sh
python3 -m http.server 4173 --bind 127.0.0.1
```

Open:

```text
http://127.0.0.1:4173/indexes/index(PMD-Rendering-Revised).html
```

## Hosting implication

If you want to self-host the full experience, hosting just the HTML and GLBs is not enough. The splat data and several runtime dependencies are still third-party hosted and would need to be mirrored or replaced.
