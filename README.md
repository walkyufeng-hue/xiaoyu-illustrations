# Xiaoyu Illustrations

> 小玉淡彩手绘速写 · 中文正文配图 Skill
>
> 把文章里的判断、流程、状态和隐喻，画成一张张干净、清爽、有速写灵气的 16:9 手绘小图。

---

![小玉淡彩手绘正文配图示例](assets/cover.png)

---

## 这个项目

我做中文内容写作，公众号长文、方法论文、读书笔记经常需要配图。

通用插画风格不稳定，正式信息图又太像汇报材料。所以我搭了这套配图方案：**先用一个固定角色「小玉」、一套固定的淡彩手绘速写风格，把文章里值得画的那个认知点画成图。**

它产出的不是"好看的装饰图"，而是文章内容本身的一个画面：一个判断、一条流程、一组对比、一个隐喻——一张图讲清楚一件事，放进正文里能帮读者 1 秒 get 到重点。

---

## 小玉是谁

小玉是这套图的固定主角，也是整套视觉的识别点：

- 年轻女性，长直发，头顶常架着一副墨镜
- 米色工装马甲，内搭黑色长袖
- 以淡彩速写呈现：有自然肤色、柔和阴影，保留铅笔/水彩笔触
- 神情平静克制，不卖萌、不夸张——像一个认真在处理眼前麻烦的普通人

小玉不做成照片、3D 渲染或卡通吉祥物。她负责**参与画面里的核心动作**，而不是站在旁边当装饰。

---

## 风格要点

- **干净背景**：纯白或接近透明为主，可有极淡投影；不要复杂场景、纹理墙面、渐变
- **淡彩手绘速写**：线条有轻重变化、不完全平滑；上色像水彩薄涂，饱和度低
- **柔和体积**：允许轻微明暗和阴影让画面有厚度，拒绝重阴影、强对比、照片级写实
- **留白**：主体占画面约 40%-60%
- **中文标注克制**：最多 5-8 处，每处 2-8 个字；红=重点批注、橙=主流向、蓝=补充说明
- **一张图一件事**：只表达一个核心动作、结构、状态或隐喻，小玉必须承担核心动作

整体感觉：清爽、自然、有生活感、有速写灵气；怪诞但不突兀，不幼稚、不商业。

---

## 示例效果

下面 5 张配图来自同一篇 PRD 反思长文（《PRD 越写越长，是产品经理在偷懒》），用本 skill 一次性生成。

### PRD 写得满但说不清

![PRD 写得满但说不清](examples/images/01-prd-overfull-not-clear.png)

### 设计与 PRD 思考方式的差异

![设计与 PRD 思考方式的差异](examples/images/02-design-vs-prd-thinking.png)

### MVP 被塞太满

![MVP 被塞太满](examples/images/03-mvp-overloaded.png)

### 三个桶的取舍：必须做 / 以后加 / 暂时不要

![三个桶的取舍](examples/images/04-three-buckets.png)

### 靠演示把 PRD 砍下来

![靠演示把 PRD 砍下来](examples/images/05-prd-trimmed-by-demo.png)

这些图片是风格校准样例，不是构图模板。使用时应该从当前文章重新发明隐喻，不要照抄这张样例的物件和构图。

---

## 安装与使用

把 `xiaoyu-illustrations/` 子目录（skill 本体）安装到 Codex skills 目录：

```bash
git clone <repository-url>
cd xiaoyu-illustrations
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
cp -R ./xiaoyu-illustrations "${CODEX_HOME:-$HOME/.codex}/skills/"
```

### 常用用法

**配图规划**（先不画，输出 shot list）：

```text
Use $xiaoyu-illustrations 先不要生图。
请分析下面这篇文章哪里值得配图，输出 5 张左右的 shot list。
每张图写清楚：放在哪段后、主题、核心意思、结构类型、小玉在做什么、建议中文标注词。

<粘贴文章>
```

**直接生成正文配图**：

```text
Use $xiaoyu-illustrations 把下面这篇文章生成 4 张小玉淡彩手绘正文配图。
要求：16:9 横版、干净背景、淡彩手绘速写、少量红橙蓝中文手写批注。

<粘贴文章>
```

**为单个观点配一张图**：

```text
Use $xiaoyu-illustrations 为"信任不是喊出来的，而是一块证据一块证据铺过去"生成一张正文配图。
画面要自然、清爽、有速写灵气，小玉必须承担核心动作。
```

**改图**（去掉多余标题或错字）：

```text
Use $xiaoyu-illustrations 帮我编辑这张图，去掉左上角的"流程图"标题，其他内容保持不变。
```

更多 prompt 示例见 [examples/prompts.md](examples/prompts.md)。

---

## 目录结构

```text
.
├── README.md
├── LICENSE
├── examples/
│   ├── images/
│   │   ├── 01-prd-overfull-not-clear.png
│   │   ├── 02-design-vs-prd-thinking.png
│   │   ├── 03-mvp-overloaded.png
│   │   ├── 04-three-buckets.png
│   │   └── 05-prd-trimmed-by-demo.png
│   └── prompts.md
└── xiaoyu-illustrations/
    ├── SKILL.md
    ├── agents/
    │   └── openai.yaml
    ├── assets/
    │   └── examples/
    └── references/
        ├── style-dna.md
        ├── xiaoyu-ip.md
        ├── composition-patterns.md
        ├── prompt-template.md
        └── qa-checklist.md
```

真正需要安装到 Codex 的是 `xiaoyu-illustrations/` 子目录；根目录的 README、LICENSE、examples 是 GitHub 分享文档。

---

## 使用提醒

- 图片里的中文文字越短越稳定；文字一多就容易被画错。
- 每张图只讲一个核心结构，别把文章做成说明书。
- 小玉必须承担核心动作；如果去掉小玉画面仍然成立，说明小玉太装饰了。
- AI 生成后检查错字、幻觉标签和多余标题，必要时减少标注重生成。

---

## License

MIT License. See [LICENSE](LICENSE).
