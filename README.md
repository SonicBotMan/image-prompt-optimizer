# Image Prompt Optimizer 🎨

> AI 图像提示词优化器 - 完全自包含

为主流 AI 图像生成工具生成专业优化的提示词，主打 Kolors (快手可灵) 和 Qwen-img (阿里千问)，同时支持 Midjourney、Stable Diffusion、DALL-E 等。

## ✨ 特性

- 🎯 **智能优化** - 自动生成专业级提示词
- 🌏 **双语支持** - 中英文双语输出
- 📱 **多平台支持** - Kolors / Qwen / Midjourney / SD
- 📚 **内置参考** - 关键词库、模板库已内置，无需外部文件
- 💡 **详细分解** - 提示词各部分详细解释

## 🚀 快速开始

### OpenClaw 用户

将 skill 添加到 workspace：

```bash
cp -r image-prompt-optimizer ~/.openclaw/workspace/skills/
```

重启 OpenClaw 后即可使用。

### 手动使用

直接参考 SKILL.md 中的指南生成提示词。

## 📖 使用方法

当需要生成或优化提示词时，直接告诉宇华，例如：

- "帮我生成一个古风少女的提示词"
- "优化这个提示词：..."
- "创建一个赛博朋克城市的提示词"

## 📦 项目结构

```
image-prompt-optimizer/
├── SKILL.md           # 主技能文件（完全自包含）
├── README.md          # 本文件
├── VISION.md          # 项目愿景
├── CONTRIBUTING.md    # 贡献指南
├── SECURITY.md        # 安全说明
└── LICENSE            # MIT 许可证
```

## 🔧 平台支持

| 平台 | 状态 | 说明 |
|------|------|------|
| Kolors | ⭐ 主推 | 快手可灵，中文优化 |
| Qwen-img | 🌟 备选 | 阿里千问，高分辨率 |
| Midjourney | 📸 支持 | --ar, --s 参数 |
| Stable Diffusion | 🎨 支持 | 采样器、CFG 建议 |

## 📚 内置资源

- ✅ 质量关键词库
- ✅ 光线关键词库
- ✅ 构图关键词库
- ✅ 风格关键词库
- ✅ 提示词模板库
- ✅ 平台特定指南

所有参考资料已内置于 SKILL.md，无需外部文件。

## 🤝 贡献

欢迎提交 Issue 和 PR！

## 📜 许可证

MIT License
