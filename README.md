# Extend Photo Travel Poster

一个面向 Codex / ChatGPT 图像编辑工作流的 Skill：把旅行、街景、建筑或自然照片制作成“上方实景 + 下方象牙白留白 + 局部钢笔线稿 + 微型人物故事”的 3:4 竖版作品。

它强调保留原照片的摄影主体、空间关系、光线与色彩，只让一个真实存在的景物自然延伸到纸面。它不会默认套用大标题、坐标、路线图、邮票或满版建筑速写等常见旅游海报模板。

## 特点

- 保留真实照片作为视觉主体
- 从道路、水面、桥梁、台阶、山坡或建筑轮廓中只选择一个元素延伸
- 使用暖白象牙纸面与大量留白
- 加入一个受力合理的微型钢笔线稿人物
- 自动选择一句 1–5 个英文单词的手写旁白
- 内置五张布局与笔触参考图，避免风格漂移
- 默认输出 3:4 竖版，可按用户要求调整

## 安装

```bash
git clone https://github.com/245331830gao-alt/extend-photo-travel-poster.git \
  ~/.codex/skills/extend-photo-travel-poster
```

重新启动或刷新 Codex 后，可在对话中调用：

```text
使用 $extend-photo-travel-poster，把上传照片做成实景延伸线稿旅行海报。
```

## 目录结构

```text
extend-photo-travel-poster/
├── SKILL.md
├── agents/
│   └── openai.yaml
├── assets/
│   ├── icon.svg
│   └── style-reference-01.jpeg ... style-reference-05.jpeg
└── references/
    ├── prompt-template.md
    ├── scene-guide.md
    └── style-anchors.md
```

## 设计边界

该 Skill 的目标不是把照片重绘成插画，也不是生成传统旅游宣传海报。以下内容默认禁止：

- 大中文地名、书法标题和大型英文副标题
- 坐标、指南针、地图路线、定位点、邮票和日历
- 中央小照片窗口与四周满版建筑速写
- 装饰性水彩飞溅、密集排线和无支撑的悬浮人物

详细规则请参阅 [SKILL.md](SKILL.md)。

## 使用与隐私

- 请只处理你拥有权利或已获授权使用的照片。
- Skill 本身不会上传仓库中的示例之外的任何图片；实际图片如何处理取决于你使用的图像生成工具和服务。
- 参考图只用于布局、留白、过渡、笔触和人物尺度，不应复制其中的具体建筑、人物或文字。

## License

[MIT](LICENSE)

---

## English

This Codex / ChatGPT skill turns travel and documentary photographs into quiet 3:4 editorial artworks: a preserved photographic scene on top, ivory paper below, one naturally extended scene element, a tiny pen-drawn character, and a short handwritten English aside.

Install the repository under `~/.codex/skills/extend-photo-travel-poster`, refresh Codex, then invoke `$extend-photo-travel-poster` with an uploaded image. See [SKILL.md](SKILL.md) for the full behavior and constraints.
