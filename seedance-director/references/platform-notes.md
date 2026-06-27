# Platform Notes

Use this file when platform behavior, references, or specs affect the prompt. Specs change; if the user asks for latest limits, verify official docs before answering.

## Verified Sources Used When Creating This Skill

- BytePlus ModelArk page title found for an official Seedance 2.0 series prompt guide; page metadata observed with updated time `2026-06-22T08:39:02Z`.
- BytePlus ModelArk search result for "Seedance-1.0-pro&pro-fast prompt guide" reports last updated June 16, 2026.
- BytePlus ModelArk video generation API search result reports last updated June 25, 2026.
- YouMind-OpenLab `awesome-seedance-2-prompts` repository was checked locally on 2026-06-26; README reports thousands of curated prompts, categories such as cinematic, anime, UGC, ads, meme styles, and a last-updated timestamp of 2026-06-26T08:13:50.389Z in the cloned copy.
- The original `songguoxs/seedance-prompt-skill` Claude Code skill was inspected as design inspiration for workflow, reference syntax, video extension, and multi-shot structure.

## Common Capabilities To Assume

Seedance-style workflows commonly include:

- Text-to-video
- Image-to-video
- Video-to-video or video editing
- Video extension
- Multimodal references: image, video, audio, and text
- Short clip generation in the 4-15 second range
- Native or prompted sound design depending on access surface

Do not promise a capability unless the user's target surface supports it. App UIs, BytePlus ModelArk API, and third-party wrappers can expose different controls.

## Reference Handling

For Chinese-language app UIs that expose uploaded assets with Chinese labels, use:

- `@图片N` for image references
- `@视频N` for video references
- `@音频N` for audio references

For API-oriented prompts, neutral labels like `reference image 1` may be clearer, but keep the copyable prompt human-readable.

Always assign each reference a job:

- Subject identity
- Wardrobe
- Product detail
- Scene or background
- First frame
- End frame
- Motion/choreography
- Camera movement
- Editing rhythm
- Audio mood or beat
- Voice timbre

## Practical Limits

Use these only as rough planning assumptions unless just verified:

- Single generations are usually short-form, often up to around 15 seconds.
- Multimodal workflows often support multiple images, a small number of videos, and a small number of audio files.
- High-quality references matter more than many references. Prefer fewer, well-assigned assets.
- Realistic human face uploads may be restricted by some app surfaces and safety filters.

If exact file count, file size, duration, model name, price, or region availability matters, browse official platform docs before answering.

## Prompt Length Heuristic

- 4-8 seconds: one focused paragraph, one action, one camera move.
- 9-12 seconds: 2-3 beats, maybe timestamps.
- 13-15 seconds: timestamped beats are recommended.
- More than 15 seconds: split into segments, use video extension, or plan post-production stitching.

## Current Community Patterns Observed

Recent high-performing community prompts often use:

- Long timestamped 15-second prompts for cinematic/drama/action scenes.
- Very explicit style blocks: `[Style]`, `[Scene]`, `[Character]`, `[Shot Details]`.
- Camera and lens specificity: macro, low angle, dolly, slow push-in, overhead, handheld, telephoto feel.
- Micro-motion realism: blinking, breathing, hair movement, finger tremble, steam, dust, water droplets.
- Consistency clauses: face, clothing, hairstyle, product geometry, logo/packaging.
- Negative prompts: no subtitles, no watermark, no extra text, no warped faces/hands, no unwanted medium.
- Clear reference-image instructions: "use storyboard only for composition, not final style."

Use these patterns selectively; do not make every prompt excessively long.
