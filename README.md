# AI Video Director

AI Video Director is a Codex skill for creating controllable prompts for general AI video generation.

AI Video Director 是一个面向通用 AI 视频生成平台的 Codex 视频提示词技能，用来生成更稳定、更可控、更像导演分镜的 AI 视频提示词。

## 中文介绍

AI Video Director 不只是帮你写“画面很美”的提示词，而是把视频提示词写成更接近导演、美术、摄影和演员调度的说明。它会补充专业镜头语言、焦距、景深、空气透视、丁达尔效应、体积光、场景空间结构、固定物与运动物关系，以及人物表演细节，帮助减少建筑漂移、场景突变、人物动作空泛、镜头逻辑混乱等常见问题。

适用于修仙仙境、天宫建筑、短剧分镜、产品广告、图生视频、视频延长、参考图/视频/音频组合、视频提示词反推等场景。

## English Introduction

AI Video Director does more than write decorative video descriptions. It turns video prompts into practical directing notes that combine cinematography, production design, spatial blocking, and character performance. It adds professional cinematic language, focal length, depth of field, atmospheric perspective, Tyndall effect, volumetric light, stable scene topology, fixed and moving object relationships, and detailed actor-performance cues to reduce common generation issues such as drifting architecture, sudden scene changes, vague character motion, and incoherent camera movement.

It is useful for fantasy cultivation scenes, heavenly palaces, short drama storyboards, product ads, image-to-video prompts, video extension, multimodal reference prompts, and reverse-engineering prompts from existing videos.

## 特点 / Features

- 专业影像术语：自动补充焦距、景深、空气透视、丁达尔效应、体积光、低机位、跟拍、视差等关键词。
- 场景结构稳定：明确前景、中景、远景、左右空间、固定物、可运动元素，降低建筑突然出现、漂移、变形的问题。
- 人物表演细节：补充姿态、步态、视线、手部动作、表情、呼吸、衣摆和发丝运动。
- 精简短句版：可以输出更适合直接复制到视频生成平台的精简中文提示词。
- 导演分镜版：可以输出更完整的时间轴、镜头、动作、声音和禁用项。
- 多模态参考：支持 `@图片1`、`@视频1`、`@音频1` 的职责分配。
- 视频反推：可以根据已有视频或关键帧，拆解风格、镜头、角色、场景和提示词结构。
- 失败修正：适合修复“太像 CG”“人物不稳”“建筑乱变”“镜头乱跳”“路人抢主体”等问题。

## Install

Copy the `ai-video-director` folder into your Codex skills directory.

Windows:

```powershell
Copy-Item -Recurse .\ai-video-director "$env:USERPROFILE\.codex\skills\ai-video-director"
```

macOS/Linux:

```bash
cp -R ./ai-video-director ~/.codex/skills/ai-video-director
```

Restart Codex after installation.

## 使用方法 / Usage

Invoke the skill in Codex with `$ai-video-director`.

```text
$ai-video-director 给我一个10秒竖屏修仙天宫散步视频提示词
```

```text
$ai-video-director 把这个视频反推成可直接使用的视频提示词
```

```text
$ai-video-director 给我一个图生视频提示词，@图片1是人物，@图片2是建筑，@图片3是云海氛围
```

```text
$ai-video-director 帮我把这个提示词改得更像真人实拍，不要游戏CG感
```

## 常用输出模式 / Common Output Modes

- `精简短句版`: concise prompt designed for direct paste into AI video platforms.
- `导演分镜版`: fuller prompt with timeline, camera movement, performance, scene layout, and constraints.
- `图生视频版`: assigns each image reference a clear job, such as subject identity, architecture, first frame, or atmosphere.
- `视频延长版`: writes continuation prompts that preserve the previous video's final frame and motion continuity.
- `视频反推版`: analyzes an existing video and produces a reproduction prompt plus a shorter practical version.
- `失败修正版`: rewrites prompts to reduce drift, pop-in, deformation, vague motion, or unwanted visual style.

## Example

```text
$ai-video-director 给我一个10秒竖屏天宫仙境视频提示词，镜头从角色身后跟拍，建筑空间稳定，有路人走动，真人实拍感
```

The skill will add details such as:

- `35mm自然叙事视角`
- `稳定器背后跟拍`
- `空气透视`
- `丁达尔效应`
- fixed foreground / midground / background layout
- fixed buildings and moving cloth, hair, clouds, dust, and passersby
- posture, gait, gaze, hands, breathing, and robe movement

## Structure

```text
ai-video-director/
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
