# Queryable Gaussian View Index

Project page and lightweight browser demo for **Queryable Gaussian View Index:
Retrieval, Localization, and Agentic View Search** (2026), by Tianyu Xiong,
Rui Li, and Jiaqi Yang.

Project page: https://six-bit-tx.github.io/qgvi-project/

## Run locally

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Open http://127.0.0.1:8000/. No build, model API, GPU, or extra runtime package
is needed. Serve over HTTP rather than opening index.html directly, because
browsers restrict fetching JSON from file URLs.

## Demo scope

- Text search runs actual BM25 on 78 selected captioned views from nine scenes.
  It is a small demonstration index, not the full evaluation database.
- RGB examples replay saved geometric localization decisions.
- Agentic view search replays eight saved decisions and observations, including
  unsuccessful proposals. It does not run live model inference or rendering.
- Camera downloads preserve native scene coordinates. Intrinsics refer to
  original source dimensions, not the resized display thumbnail.

The paper PDF includes supplementary material and the latest matched
agentic controls. Model-assessed semantic results, development-set scope,
and estimated metric scales are disclosed on the page and in the paper.

See assets/credits.txt for image and dataset credits. This repository contains
website source and demonstration assets, not the full research implementation.
No new license is assigned here to the underlying third-party scene assets.

The site is served by GitHub Pages directly from this branch's root.
All asset URLs are relative, so the page works under the project URL path.
