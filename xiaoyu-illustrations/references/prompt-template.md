# 生图提示词模板

每张图单独生成。根据正文内容替换变量，不要把多张图拼在一起。

```text
Generate one standalone 16:9 horizontal Chinese article illustration.

Visual DNA:
Clean white or transparent background. Soft hand-drawn illustration in muted watercolor/sketch style, with visible pencil-style line work and gentle light shading. Low-saturation natural colors. Breathing room with plenty of empty space. Sparse red/orange/blue handwritten Chinese annotations. Fresh, understated, slightly absurd explanatory-sketch feeling. No heavy shadows, no photorealism, no 3D render, no gradients, no complex background, no commercial vector style, no PPT infographic look, no cute mascot poster, no children's illustration, no realistic UI.

Recurring IP character required:
小玉 (Xiaoyu), a young woman with long straight hair, sunglasses resting on top of her head, wearing a beige/khaki utility vest over a black long-sleeve top and white undershirt, with a delicate necklace, small earrings, a smartwatch and bracelets. Drawn as a soft hand-drawn watercolor/sketch figure with natural skin tone, muted clothing colors, gentle shading, and visible pencil line texture on a clean white background. Not a photorealistic portrait, not a black-line icon, not cute, not a mascot. Xiaoyu must perform the core conceptual action, not decorate the scene. Make Xiaoyu calm, focused, and slightly deadpan, not cute.

Theme:
{正文配图主题}

Structure type:
{结构类型：Workflow / 系统局部 / 前后对比 / 角色状态 / 概念隐喻 / 方法分层 / 地图路线 / 小漫画分镜}

Core idea:
{这张图要表达的核心意思}

Composition:
{具体画面：小玉在哪里、正在做什么、主要物件是什么、信息如何流动}

Suggested elements:
{元素1} / {元素2} / {元素3} / {元素4}

Chinese handwritten labels:
{标注词1} / {标注词2} / {标注词3} / {标注词4} / {可选标注词5}

Color use:
Natural muted tones for Xiaoyu's skin, hair, and clothing. Black/deep gray for main outlines, structure, and key text. Orange for main flow/path/arrows. Red only for key warnings/problems/results. Blue only for secondary notes or feedback/system state.

Constraints:
One image explains only one core structure. Keep the main subject around 40%-60% of the canvas. Preserve at least 35% blank white space. Use at most 5-8 short handwritten Chinese labels. Do not write a title in the top-left corner. Do not write the structure type on the image. Do not make it a formal diagram, course slide, or dense explainer. Do not copy prior examples or reuse known case compositions unless explicitly requested; invent a fresh visual metaphor for this specific article. It should be clear but not instructional, interesting but not childish, strange but clean.
```

## 图像编辑提示

去掉左上角标题：

```text
Edit the provided image. Remove only the handwritten title "{要删除的文字}" and its underline from the top-left corner. Fill that area with the same clean white background, matching the surrounding blank paper. Preserve everything else exactly: characters, labels, paths, line style, composition, aspect ratio, and image quality. Do not add any new text or objects.
```

增强怪诞感：

```text
Regenerate this illustration with the same core meaning and simple layout, but make Xiaoyu more central to the conceptual action. Xiaoyu should be doing the strange work that explains the idea, not standing beside the diagram. Keep it clean, sparse, softly colored with muted watercolor/sketch style, and not cute.
```
