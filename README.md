# LandV project page

Static research website for *LandV: Multimodal World Modeling for Autonomous Driving via Modality-Aligned Asymmetric Dual-Stream Architecture*.

## Preview

From the repository root, run:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Open `http://127.0.0.1:8000/`.

## GitHub Pages

Publish the repository root from the `main` branch in **Settings → Pages → Deploy from a branch**. All media, images, and fonts use paths relative to the page. [GitHub Pages publishing sources](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)

## Editing

- The author byline belongs below the title in `index.html`. The two result tables are plain HTML.
- Video categories, scene identifiers, and captions are in `site.js`. The nine gallery videos use a 12 Hz time base. The gallery defaults to one-third speed and also supports original speed.
- The opening comparison shows GT and original generation, followed by left and right turns from the same measured RGB and LiDAR frame in `scene-0524_208` (commanded yaw +25° and −25°, seed 2026112704). The first frame shows the input and the next 16 are model predictions in the generated views. The left turn approaches the white SUV and the right turn approaches the parked sedan.
- The bottom pair uses the same observed first frame and sampling noise. The left panel repeats the original prediction. The right adds a moving 3D box for a sedan passing on the left. Its location is empty in the measured first frame. The generated sedan first appears at the edge of the rear-left view around t2, passes the front-left camera, and enters the front view around t10.
- Drag any divider to reveal RGB or LiDAR across all six panels. The shared 17-frame source, `assets/videos/hero-controls.mp4`, packs six 1040 × 300 strips alternating RGB and LiDAR. Its poster uses the same layout.
- The page organization was informed by [Drive-WM](https://drive-wm.github.io/). Font licenses are included in `assets/fonts/`.
