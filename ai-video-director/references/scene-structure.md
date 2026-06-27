# Scene Structure

Use this file when a video contains architecture, rooms, streets, vehicles, crowds, products, fantasy spaces, or anything that must remain physically stable.

## Goal

Make the model treat the scene as a fixed physical space, not a changing collage.

Always define:

- fixed layout
- camera path
- character path
- foreground/midground/background
- left/right/front/rear relationships
- fixed objects
- moving objects
- allowed reveal mechanism
- forbidden spatial errors

## Core Template

```text
场景空间固定：前景为[主体/路径/近处物体]，中景为[左右环境/人群/回廊]，远景为[主建筑/目标点]。左侧固定为[左侧元素]，右侧固定为[右侧元素]，正前方固定为[远景目标]。镜头沿[路径]运动，只因镜头前进、遮挡打开、转过拐角或视差变化而逐渐显露更多细节。固定不动：[建筑、道路、栏杆、柱子、门、产品底座]。可运动：[人物、衣摆、头发、雾气、云层、水流、灯火、尘粒]。禁止建筑凭空出现、漂移、变形、消失、左右互换或尺度忽大忽小。
```

## Follow-Behind Architecture Template

```text
镜头从角色身后直接开始，角色沿中央[石阶/长廊/街道/桥面]向前走，背影保持在画面下中部。左侧是[固定回廊/墙体/柱列]，右侧是[栏杆/云海/店铺/河道]，远处[主殿/城门/塔楼]始终固定在正前方。镜头稳定器背后跟拍，随着角色前进产生真实视差，近处柱子和路人从画面两侧经过，远处主建筑只逐渐变大，不突然改变位置。
```

## Crowd Blocking

For passersby or crowds, specify:

- quantity: few, scattered, dense, ceremonial line
- position: left corridor, far steps, side market, background plaza
- motion direction: crossing left-to-right, walking toward camera, walking away, standing still
- behavior: low-key, avoiding protagonist, looking up, carrying lanterns
- hierarchy: they must not steal focus from the main subject

Example:

```text
少量古装路人自然走动：两三人从左侧回廊经过，一人提灯从右侧栏杆旁走远，远处几人停步仰望主殿。路人动作克制，不抢主体，与主角保持自然避让关系。
```

## Reveal Rules

Use these when the user complains about things appearing from nowhere:

- "新建筑只因镜头前进后被廊柱遮挡解除而进入画面"
- "远处主殿从开场就存在，只是被薄雾和柱廊部分遮挡"
- "建筑位置、大小比例和朝向全程稳定"
- "镜头运动只改变视角和遮挡关系，不改变场景拓扑"
- "不要在角色旁边突然生成新的宫殿或栏杆"

## Product / Object Layout

For product videos:

```text
产品固定在画面中央转台上，背景为[固定场景]。镜头环绕产品，产品位置不漂移；可运动元素只有水珠、包装反光、烟雾、光斑和产品旋转。禁止产品形状变化、logo漂移、部件凭空出现。
```

## Interior Layout

For rooms:

```text
房间布局固定：左侧为窗户和书桌，右侧为木门和屏风，远景为床榻，中央为空地。角色从门口走向窗边，镜头横移跟随。家具位置不变，只因角色和镜头移动改变遮挡关系。
```

## Checklist

Before final prompt:

- Is there a clear path for the camera?
- Is there a clear path for the subject?
- Does the prompt say what stays fixed?
- Does the prompt say what can move?
- Does the prompt forbid pop-in, drift, deformation, and side swapping?
- Are passersby blocked without stealing the main focus?
