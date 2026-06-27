# Quality Checklist

Use this before returning an AI video prompt.

## Copyability

- The main prompt can be copied directly into the target platform.
- Reference labels match the user's assets and are not skipped or duplicated.
- If there are several versions, each version is self-contained.

## Visual Specificity

- Subject, scene, lighting, action, and final frame are concrete.
- Motion has order and cause: first this happens, then that happens.
- Camera language is named: push-in, pull-back, pan, tilt, track, orbit, handheld, overhead, low angle, close-up, macro.
- Style is not just "cinematic"; it includes texture, color, lighting, lens feel, or production reference.
- Professional terms are used when helpful: focal length, lens feel, depth of field, atmospheric perspective, Tyndall effect, volumetric light, parallax, blocking, material texture.
- Terms are not dumped randomly; each one has a visible purpose.

## Scene Structure

- Foreground, midground, and background are clear when the scene has depth.
- Left/right/front/rear relationships are clear for architecture, streets, rooms, or crowds.
- Fixed objects are named: buildings, doors, stairs, railings, columns, product base, furniture.
- Moving objects are named: main character, passersby, cloth, hair, smoke, clouds, water, dust, light particles.
- Camera movement explains why new details enter the frame.
- Prompt forbids sudden pop-in, drifting buildings, deformation, disappearing structures, scale jumps, and left/right swaps when relevant.

## Consistency

- Character/product identity is explicitly preserved where needed.
- Wardrobe, face, hairstyle, product geometry, and logo behavior are called out.
- If using multiple references, each reference has exactly one or more clear jobs.

## Human Performance

- Dialogue uses role, emotion, and quoted lines.
- Lip sync requests are natural and restrained.
- Micro-expressions, breath, gaze, blinking, and hand gestures support the scene.
- Avoid exaggerated facial motion unless the style requires it.
- People have posture, gait, gaze, hand behavior, expression, breathing, and cloth/hair motion when they matter.
- Background people have simple blocking and do not steal focus.
- For follow-behind shots, the character remains consistent in back view and side/back profile.

## Sound

- Ambient sound, Foley, music, beat sync, and dialogue are separated when complex.
- For music videos or ads, specify how the visual rhythm follows the beat.
- If no audio is desired, state no dialogue, no narration, no BGM.

## Negative Constraints

Add only relevant negatives. Common items:

- no subtitles
- no extra text
- no watermark
- no logo unless specified
- no distorted hands
- no warped faces
- no identity drift
- no sudden scene jump
- no unwanted photorealism/anime/3D style

## Long Video Integrity

For segmented outputs:

- Each segment is no longer than the practical generation length.
- Each later segment says to upload the previous result as `@视频1` or the user's chosen label.
- Each segment has a handoff frame that exactly describes the last visual state.

## Final Response Shape

- If the user asked for just a prompt, lead with the prompt, not theory.
- Explain choices only after the copyable prompt.
- Offer 1-3 optional variations only when genuinely useful.
