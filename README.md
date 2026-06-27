# Seedance Director

Seedance Director is a Codex skill for writing controllable video prompts for Seedance / Dreamina / 即梦.

It focuses on practical prompt control rather than decorative wording:

- cinematic and photographic terminology with plain-language intent
- stable scene topology for architecture, crowds, interiors, products, and fantasy spaces
- character performance details such as posture, gait, gaze, hands, breathing, cloth, and hair motion
- image/video/audio reference assignment using `@图片1`, `@视频1`, and `@音频1`
- prompt reverse-engineering from existing videos or frames
- concise 即梦短句版 and fuller director-style prompt formats

## Install

Copy the `seedance-director` folder into your Codex skills directory.

Windows:

```powershell
Copy-Item -Recurse .\seedance-director "$env:USERPROFILE\.codex\skills\seedance-director"
```

macOS/Linux:

```bash
cp -R ./seedance-director ~/.codex/skills/seedance-director
```

Restart Codex, then invoke:

```text
$seedance-director 给我一个10秒竖屏修仙天宫散步视频提示词
```

## Structure

```text
seedance-director/
  SKILL.md
  agents/openai.yaml
  references/
    cinematic-terms.md
    scene-structure.md
    character-performance.md
    prompt-patterns.md
    quality-checklist.md
    platform-notes.md
```

## License

MIT
