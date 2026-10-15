# Relay log

## Batch 1 — complete — 16 October 2026

- Status: delivered C01–C12 and S01–S06; no failed or skipped assets.
- Asset commit SHA: `50ce2899579758a69b77ae3b6c028fdc75f28ec8` on `main`. This resolved hash identifies the asset commit; a subsequent log-only commit records it here.
- Conservative estimated generation cost: **US$13.50**, including four rejected successful generations. This is a published-tariff estimate, not an invoice; taxes and credits are excluded. See `costs/batch-1.json`.
- Delivery: 12 silent five-second 1920×1080 H.264/yuv420p clips at 24 fps, CRF 22, faststart; six native 2048×1152 WebP stills; 18 previews and a batch contact sheet. Every file is under 12,000,000 bytes; no Git LFS.
- Models: Runway Gen-4.5, Kling Video 3.0 Pro, and FLUX.2 Max via official-model prediction endpoints. Kling does not expose a seed; those manifest entries use null.
- Retries: C01 (literal circuit traces instead of organic liquid); C05 (capsule-like object and label-like marks); C08 (faint identification-like marks on a packaged chip); C09 (small signature-like marks). Each was regenerated once, and rejected originals are excluded from the repository. Costs are included in the per-asset manifest totals.
- Substitutions/limitations: C04 uses nonlinguistic geometry instead of mathematical writing; C06 uses abstract phosphor noise instead of glyphs to honor the global no-text/no-UI rule. C08 is stylized exposed circuitry; literal bare-die geometry is approximate. Some shots favor cel shading, others practical macro textures.
- Validation: complete decode check for every clip; codec, dimensions, pixel format, frame rate, 120-frame duration, no audio, faststart atom order, file sizes and still formats verified. Start/middle/end frames of all clips and the still contact sheet were visually inspected; C05's first lattice was also checked at 1.4 seconds. No visible writing, logos or signatures were observed in the accepted sampled frames. Credentials were checked out of all public files.

Batch 2 is being prepared separately and will be added above this entry.
