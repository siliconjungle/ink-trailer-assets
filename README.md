# ink trailer assets

Visual assets generated on Replicate for a one-minute trailer for **ink**, a programming language.

- `clips/`: silent five-second, 1920×1080 H.264 MP4s, 24 fps, yuv420p, CRF 22, faststart.
- `stills/`: native 2048×1152 WebP images.
- `thumbs/`: 960-pixel-wide previews; clip thumbnails use the middle frame. `contact-sheet.jpg` includes all assets.
- `manifest.json`: prompts, models, requested seeds, dimensions, sizes, and estimated generation cost per asset.
- `RELAY.md`: batch status, asset commit, substitutions, and failures.

All repository files are below 12,000,000 bytes. Git LFS is not used. No API credentials are included.

## Models and costs

Model selection and prices were checked on Replicate on 16 October 2026:

- [Runway Gen-4.5](https://replicate.com/runwayml/gen-4.5): practical and macro sequences, $0.12 per output second. Native source resolution is recorded per clip; delivery uses Lanczos scaling to 1080p.
- [Kling Video 3.0 Pro](https://replicate.com/kwaivgi/kling-v3-video): selected stylized environments and the core, native 1080p without audio, $0.224 per output second. The model does not expose a seed input.
- [FLUX.2 Max](https://replicate.com/black-forest-labs/flux-2-max): stills, $0.04 per run plus $0.03 per output megapixel. Still estimates conservatively round output megapixels up to a whole number.

Costs in the manifest are estimates based on published tariffs, before taxes or credits; they are not a retrieved invoice. Any billed rejected generations are included in the batch ledger. All predictions use the official-model endpoint, `POST /v1/models/{owner}/{name}/predictions`.

The requested mathematical marks and unreadable terminal glyphs are rendered as nonlinguistic geometry and phosphor noise to satisfy the global no-text/no-UI direction. Tiny anonymous silhouettes are used only where requested. There are no named franchise or artist references in the prompts.

## Encoding

```sh
ffmpeg -i source.mp4 -map 0:v:0 -an \
  -vf 'scale=1920:1080:flags=lanczos,setsar=1,fps=24' -t 5 \
  -c:v libx264 -preset slow -crf 22 -pix_fmt yuv420p \
  -movflags +faststart output.mp4
```

Generated imagery is probabilistic. See `RELAY.md` for the visual inspection and any limitations specific to this batch.

## Batch 2 — natural history and darkfield microscopy

`B01`–`B09` are generated natural-history/microscopy illustrations; `P01`–`P04` are Pexels stock excerpts. Batch 1 is retained. `manifest.json` is cumulative and includes a `batch` field. See `RELAY.md` for current delivery status, `costs/` for separate batch budgets, and `STOCK-CREDITS.md` for source licences. `thumbs/contact-sheet.jpg` includes all delivered assets; separate sheets preserve each batch.
