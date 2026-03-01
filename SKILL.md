---
name: image-prompt-optimizer
description: >
  生成和优化 AI 图像生成提示词，主打 Kolors (快手可灵) 和 Qwen-img (阿里千问)，同时支持 Midjourney、Stable Diffusion、DALL-E 等。
  Use when: (1) 生成图片提示词, (2) 优化现有提示词, (3) 创建提示词变体, (4) 将想法转化为详细提示词, (5) 提到 '提示词'、'画图'、'生成图片'、'prompt'、'Kolors'、'Qwen'、'Midjourney'、'Stable Diffusion'、'AI绘图'、'文生图' 等关键词
---

# AI 图像提示词优化器

为主流 AI 图像生成工具生成专业优化的提示词，**主打 Kolors (快手可灵)** 和 **Qwen-img (阿里千问)**，同时支持 Midjourney、Stable Diffusion、DALL-E 等。

## 核心工作流

当用户请求生成或优化提示词时：

1. **理解意图**
   - 识别核心主题和期望结果
   - 只有在请求极其模糊时才提问澄清
   - 默认使用合理假设而非过度提问

2. **生成全面的提示词**
   - **主格式：Kolors (快手可灵)** - 使用自然语言描述 + 中文关键词优化
   - **次格式：Qwen-img (阿里千问)** - 高分辨率，适合专业场景
   - 提供 2-3 种不同风格或方法的变体
   - 中英文双语输出
   - 对于 Kolors：使用清晰的描述性语句 + 质量关键词
   - 对于其他平台：使用公式 `[主体] + [环境] + [风格] + [光线] + [构图] + [质量]`

3. **包含平台特定优化**
   - **Kolors (快手可灵) - 主推**: 中文友好，自然语言描述，添加质量关键词
   - **Qwen-img (阿里千问) - 次推**: 高分辨率，适合专业场景，精细控制
   - Midjourney (次要): 添加 `--ar`, `--s`, `--q` 等参数
   - Stable Diffusion (次要): 建议采样步数、CFG scale 和负面提示词
   - 适配用户指定的平台，未指定时默认 Kolors

4. **解释和教育**
   - 分解提示词的每个组成部分
   - 解释为什么选择特定关键词
   - 提供修改建议以获得不同效果

5. **提供可操作的下一步**
   - 指导用户如何使用提示词
   - 建议参数调整以优化
   - 根据结果提供迭代

---

# 📚 内置关键词参考

## 质量关键词

### 基础质量
- high quality / high resolution
- detailed / highly detailed
- sharp focus / crisp
- clear / clean

### 高级质量
- 4k / 8k / ultra hd
- masterpiece
- professional
- photorealistic / hyperrealistic
- award winning
- trending on ArtStation
- best quality
- ultra detailed

## 光线关键词

### 自然光
- natural lighting / sunlight
- golden hour / blue hour
- soft lighting / harsh lighting
- backlit / rim lighting
- diffused light
- dappled sunlight
- sunrise / sunset

### 人造光
- studio lighting
- dramatic lighting
- neon lights
- candlelight / firelight
- volumetric lighting (god rays)
- spotlight
- ambient lighting

## 构图关键词

### 相机角度
- close-up / extreme close-up
- medium shot / full shot
- wide angle / panoramic
- bird's eye view / aerial view
- low angle / high angle
- eye level

### 景深
- shallow depth of field
- bokeh (blurred background)
- deep focus
- selective focus
- macro / micro

## 风格关键词

### 艺术风格
- impressionism / surrealism / minimalism
- baroque / art nouveau / expressionism
- cubism / pop art / abstract
- cyberpunk / steampunk / solarpunk

### 媒介风格
- oil painting / watercolor / acrylic
- pencil sketch / charcoal / ink drawing
- digital art / 3D render / photography
- anime / manga / comic book
- pixel art / low poly / vector art

## 情绪关键词

### 正面情绪
- peaceful / serene / calm
- magical / whimsical / dreamy
- romantic / uplifting

### 戏剧性情绪
- dramatic / intense / epic
- mysterious / atmospheric / moody
- eerie / haunting / noir

---

# 📋 提示词模板库

## 基础公式

```
[主体] + [环境] + [风格] + [光线] + [构图] + [质量]
```

## 人像模板

```
[年龄][性别]，[外貌特征]，[服装]，[表情]，[背景]，
[风格]，[光线]，portrait photography，[质量]

示例：
一位年轻亚洲女性，长发披肩，身穿休闲白衬衫，
微笑自然，户外背景，日系风格，柔和光线，
portrait photography，4k，清晰对焦
```

## 写实模板

```
[主体]，[场景]，shot on [相机型号]，[镜头]，[光线]，[后期]

示例：
山景，日落金山，shot on Canon EOS R5，
24mm镜头，自然光，HDR，专业摄影
```

## 幻想角色模板

```
[种族/职业]角色，[特征]，[装备]，[姿势]，[环境]，
fantasy art style，[氛围]，detailed，concept art

示例：
精灵战士，银甲，手持发光剑，站立姿势，
古老森林，fantasy art style，神秘氛围，
highly detailed，concept art，trending on ArtStation
```

---

# ⚙️ 平台特定指南

## Kolors (快手可灵) - 主推

- **模型选择**: Kolors 基础版 / Kolors + LCM 加速
- **中文优化**: 对中文支持优秀，直接用中文描述
- **特色**: 色彩鲜艳，细节丰富，适合中文场景
- **质量关键词**: `杰作, 高细节, 8k, 最佳质量, highly detailed`

**示例提示词**:
```
一位穿汉服的年轻女子，站在古典园林中，繁花似锦，
金色阳光透过树叶洒落，浅景深，古典油画风格，
8k，超高清，杰作，细节丰富
```

## Qwen-img (阿里千问) - 备选

- **模型选择**: qwen-t2a / qwen-img-1
- **高分辨率**: 适合 1024x1024 以上
- **特色**: 阿里千问，语义理解强，适合复杂场景
- **质量关键词**: `high resolution, photorealistic, detailed`

## Midjourney

- **参数**: `--ar 16:9` (宽高比), `--s 100` (风格化), `--q 2` (质量)
- **质量关键词**: `--q 2 --v 6`

## Stable Diffusion

- **采样步数**: 20-30
- **CFG Scale**: 7-12
- **负面提示词**: `lowres, bad anatomy, bad hands, text, error`

---

# 💡 优化技巧

## Kolors 技巧

- 使用中文描述效果更好
- 添加质量词: `杰作, 高细节, 8k, 最佳质量`
- 描述性语句而非关键词堆砌

## Midjourney 技巧

- 使用逗号分隔关键词
- 添加 `--ar` 控制比例
- 使用 `--iw` 控制原图参考程度

## Stable Diffusion 技巧

- 负面提示词很重要
- 采样器推荐: DPM++ 2M Karras
- 控制网(CN)可精确控制

---

# 📝 输出格式

按以下结构回复（优先 Kolors 格式）：

## 🎨 生成的提示词

### ⭐ 主推：Kolors (快手可灵)
**中文提示词:**
[清晰描述性语句，包含主体、环境、风格，光线、构图、质量关键词]

**英文翻译:**
[English translation]

**适用平台:** Kolors (快手可灵)
**推荐参数:** 
- 基础: Kolors
- 高质量: Kolors + LCM 加速

---

### 🌟 备选：Qwen-img (阿里千问)
**中文提示词:**
[适合高分辨率的详细描述]

**英文翻译:**
[English translation]

**适用平台:** Qwen-img (阿里千问)
**推荐参数:**
- 基础: qwen-t2a
- 专业: qwen-img-1

---

### 📸 Midjourney 风格
**英文提示词:**
[关键词风格 - Midjourney 格式]

**中文翻译:**
[中文翻译]

**适用平台:** Midjourney

---

## 📝 提示词分解

- **主体:** [解释]
- **环境:** [场景描述]
- **光线:** [使用的摄影/光影术语]
- **风格:** [视觉美学描述]
- **质量:** [4k, 8k, highly detailed 等]
- **构图:** [构图方式]

## ⚙️ 平台指南

**🌟 Kolors (主推):**
- 模型选择: [Kolors 基础版 / Kolors + LCM]
- 中文优化: 对中文支持优秀，直接用中文描述
- 特色: 色彩鲜艳，细节丰富，适合中文场景
- 质量关键词: `杰作, 高细节, 8k, 最佳质量`

**🌟 Qwen-img (备选):**
- 模型选择: [qwen-t2a / qwen-img-1]
- 高分辨率: 适合 1024x1024 以上
- 特色: 阿里千问，语义理解强，适合复杂场景
- 质量关键词: `high resolution, photorealistic, detailed`

---

