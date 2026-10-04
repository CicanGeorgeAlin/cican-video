# CICAN VIDEO GENERATOR

**V1.0 — GitHub Pages frontend**

CICAN VIDEO GENERATOR is a free/open-source-first AI video creation platform.

## Current status

The responsive generator interface is live in this repository. The interface is intentionally honest: GitHub Pages hosts the frontend but does not provide the GPU required to run the video model. Until a real generation backend is connected, **GENERATE VIDEO** reports that the engine is unavailable.

## Architecture

GitHub Pages frontend → generation API → GPU provider → open-source video model → MP4 → browser player/download.

The frontend is provider-agnostic. The API base URL will be configured when the GPU backend is deployed.

## First model target

**Wan2.1 T2V-1.3B** is the first backend candidate. It must be installed and tested on suitable GPU hardware before CICAN VIDEO GENERATOR is declared **GOLDEN BASE**.

## Free-first policy

- Open-source models first.
- Free/local GPU environments where realistically available.
- No mandatory paid video API.
- Optional paid compute may be supported later.
- Never fake a generated video or fake completion status.

## V1 frontend

- Text prompt
- 16:9, 9:16 and 1:1 controls
- Verified initial duration control: 5 seconds
- Style prompt modifier
- Generation status
- Responsive MP4 player
- Download control
- Mobile-first black/white CICAN design
- No secrets in frontend

## Next milestone

Connect a real GPU environment, install and test the selected open-source model, expose:

- `POST /api/generate`
- `GET /api/status/:job_id`

Then perform an end-to-end test that produces a real MP4.

## Roadmap

- **V1.0** — responsive generator frontend
- **V1.1** — real text-to-video
- **V1.2** — image-to-video
- **V1.3** — custom player improvements
- **V2.0** — script, scenes, voice, music and subtitles studio
