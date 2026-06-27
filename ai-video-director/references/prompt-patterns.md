# Prompt Patterns

Use this file when drafting an AI video prompt, especially for multimodal references, long scenes, ads, drama, anime, or edits.

## Universal Formula

`[duration + ratio + style] + [subject] + [scene] + [action sequence] + [camera movement] + [motion/physics details] + [audio/dialogue] + [negative constraints]`

Keep causal order obvious. The model should know what appears first, how it moves, and what the final frame should be.

For realistic video prompts, expand the formula to:

`[duration + ratio] + [realism target] + [visual terms] + [fixed scene topology] + [character performance] + [camera path] + [chronological action] + [negative constraints]`

Do not let professional terms become decoration. Each term must control something visible.

## Direct-Paste Short Prompt

Use when the user asks for a direct-paste prompt, concise version, short Chinese version, or when the idea is simple.

```text
[时长]，[比例]，[真实/动画/广告/短剧风格]。[场景结构固定：前景...，中景...，远景...，左侧...，右侧...，固定不动...，可运动...]。[主体表演：姿态、步态、视线、手部、表情、衣料/发丝运动]。[镜头从...开始，以...方式运动，只因镜头移动逐渐显露更多细节]。[专业画面控制：20mm广角/35mm自然视角/85mm长焦、空气透视、丁达尔效应、真实景深等]。禁止...
```

Keep this mode copyable: one compact paragraph or 2-3 short paragraphs, no long teaching unless the user asks.

## Reverse-Engineer From Video

Use when the user provides a video and asks what prompt should be used.

Extract:

- duration, ratio, broad style
- subject and wardrobe
- scene topology and fixed structures
- camera path and edit rhythm
- action/performance details
- lighting, lens, atmosphere, color, texture
- sound if relevant
- likely negative constraints

Return both a reproduction prompt and a shorter practical version.

## Text-Only Video

Best for original scenes with no required exact product/character identity.

Template:

```text
[时长]，[比例]，[风格和画质]。画面中[主体]在[场景]中[动作]。[镜头语言]，[光影和色彩]。[动作细节和物理细节]。[声音/音乐/对白]。禁止出现[不需要的元素]。
```

## Image-To-Video

Use when a reference image controls character, product, first frame, end frame, or composition.

Template:

```text
@图片1用于[主体/产品/首帧/构图]参考，保持[关键外观]一致。[时长]，[比例]，[风格]。从@图片1的画面开始，[主体]先[动作1]，随后[动作2]，最终停在[结尾画面]。镜头[推/拉/摇/跟拍/环绕]，光线[具体描述]。不要改变@图片1中的[不可变元素]，禁止出现文字、水印、logo、变形。
```

When using a rough sketch/storyboard, say exactly what to borrow and what to discard:

```text
参考@图片1的构图、机位和动作连续性，但最终画面必须是[完整彩色/写实/动画]风格，不保留草图线稿、黑白铅笔质感或分镜标注。
```

## Multimodal Reference

Use when images, video, and audio each control different dimensions.

Pattern:

- Image controls: identity, wardrobe, product detail, scene, first/end frame.
- Video controls: choreography, camera movement, editing rhythm, physical action, transition effects.
- Audio controls: BGM mood, beat sync, voice timbre, sound-effect rhythm.

Template:

```text
@图片1用于主体外观一致性，@图片2用于场景氛围；参考@视频1的运镜节奏和动作幅度，不保留原人物；@音频1用于BGM节奏和鼓点卡点。[完整画面和时间线]。
```

## Timestamped 15-Second Story

Use for drama, ads, MV, action, transformation, cooking, or any scene with more than two beats.

```text
15秒，[比例]，[总体风格]。[主体与场景总述]。
0-4秒：[镜头1，构图，主体动作，环境变化，声音]
4-9秒：[镜头2，运镜，动作推进，表情/物理/特效细节，声音]
9-15秒：[镜头3，高潮或结尾，最终画面，声音收束]
全程保持[主体一致性/风格一致性]。禁止[文字/字幕/logo/水印/畸形/无关元素]。
```

## One-Take Continuous Shot

Use when the user asks for 一镜到底, long take, tracking shot, continuous transition.

```text
一镜到底，[时长]，[比例]，[风格]。镜头从[起点画面]开始，以[跟拍/手持/稳定器/航拍/第一人称]方式连续移动，经过[空间节点1]、[空间节点2]、[空间节点3]，最终停在[终点画面]。全程不切镜头，不跳帧，不突然变换主体；通过[遮挡物/转身/推门/穿越光影]自然转场。声音连续，环境音随空间变化自然过渡。
```

Add fixed topology for stable spaces:

```text
场景空间固定：前景为[主体/路径]，中景为[左右环境]，远景为[主建筑/目标点]；[主建筑、廊柱、栏杆、石阶、门楼]固定不动，镜头运动只改变遮挡关系和可见范围，不允许建筑凭空出现、移动、变形或左右位置互换。
```

## Follow-Behind Character Shot

Use when the camera follows a character from behind, especially in architecture, streets, fantasy spaces, or immersive scenes.

```text
[时长]，[比例]，[风格]。镜头从角色身后直接开始，稳定器背后跟拍，保持角色背影位于画面下中部，沿[路径]向[目标]前进。场景空间固定：[左侧环境]，[右侧环境]，[远景目标]始终保持相对位置不变；新建筑和细节只因镜头前进、遮挡打开或角色转过拐角而进入画面，不允许凭空生成。角色[姿态/步态/手部/视线/表情/衣料发丝]；路人[数量、运动方向、避让关系]，不抢主体。
```

## Video Extension

Use when continuing an existing video.

```text
将@视频1向后延长[新增时长]秒。承接@视频1最后一帧的[人物姿态/物体位置/光线/镜头方向]，保持画面风格、运动速度、色调和声音连续。[新增时间线]。不要重播原片段，不要突然换场，不要改变主体身份。
```

For forward extension:

```text
将@视频1向前延展[新增时长]秒，作为原视频之前发生的内容。结尾必须自然衔接到@视频1第一帧：[第一帧状态描述]。
```

## Video Editing

Use when modifying an existing source video.

```text
编辑@视频1：将[原元素]替换/移除/增加为[@图片1或新元素]，保留原视频的[镜头节奏/动作/场景/光影]。新元素需要与原画面的透视、光照、运动模糊和遮挡关系一致。禁止改变[不可动元素]。
```

## Product Ad

Strong product prompts define materials, motion, benefit, brand-safe text behavior, and end card.

```text
[时长]产品广告，@图片1为产品外观和包装细节参考，保持logo和包装比例准确。[场景/背景]，[产品动作：旋转、爆开、凝结水珠、分解重组、使用场景]。镜头[微距/环绕/推近]，光线[高端棚拍/自然晨光/霓虹反射]。声音包含[开盖声/气泡声/机械声/轻快BGM]。如需文字，只出现[指定短句]；否则禁止任何额外文字、水印和字幕。
```

## Short Drama With Dialogue

Use compact dialogue and emotional staging. Keep mouth movement natural.

```text
[时长]竖屏短剧，[场景]，[人物关系和情绪冲突]。
0-X秒：画面...
台词（角色，语气）："..."
X-Y秒：画面...
台词（角色，语气）："..."
音效：[环境音、动作声、音乐]
要求：自然唇形同步，台词低能量真实表演，不要夸张口型，不要字幕。
```

## Anime / Stylized Video

State what style to use and what to avoid.

```text
[日式2D动画/国漫3D渲染/赛璐璐/水墨动画]风格，[时长]。[角色设计]，[场景]，[动作时间线]。线条[清晰/柔和]，色彩[明亮/低饱和/高对比]，镜头[推拉摇移]。禁止真人写实、3D塑料感、游戏引擎质感、文字、水印。
```

## Music Sync / MV

```text
@音频1作为音乐节奏参考，画面按鼓点卡点剪辑。[时长]MV，[视觉主题]。每个强拍切换[动作/构图/颜色/角色特写]，副歌处[高潮动作]。参考@视频1的剪辑节奏但不保留原内容。禁止画面与节奏脱节，禁止字幕和水印。
```

## Long Video Plan

If the requested total length exceeds a single reliable generation, split it:

```markdown
## 分段方案

### 第1段 0-15秒：正常生成
[prompt]
衔接点：最后一帧是...

### 第2段 15-30秒：上传第1段为@视频1后延长
将@视频1向后延长15秒。承接上一段最后一帧...
衔接点：最后一帧是...
```

Each segment must contain its own copyable prompt and a handoff-frame description.
