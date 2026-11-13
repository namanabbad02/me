# naman-jain-site

Personal site of Naman Jain, AI engineer. One static page, no build step.

- `index.html`: the whole site (HTML, CSS and JS in one file)
- `img/`: try-on training runs, fitting-room renders, sample leaves
- `models/plant/`: repaired EfficientNetB3 plant classifier as a TensorFlow.js graph model (float16, 22 MB), loaded only when a visitor uses the demo

Runtime dependencies, loaded from CDNs on demand: Google Fonts, `@huggingface/transformers@3.8.1` and the `Xenova/all-MiniLM-L6-v2` model (the router), `@tensorflow/tfjs@4.22.0` (the plant demo).

Run locally: `python -m http.server 8000`, then open http://localhost:8000.
Deploy: any static host. `vercel.json` sets long cache headers for `models/` and `img/`.
