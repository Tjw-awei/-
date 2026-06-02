---
language:
- zh
license: apache-2.0
tags:
- text-generation
- qwen
- qwen2
- lora
- safety
base_model: Qwen/Qwen2.5-0.5B
pipeline_tag: text-generation
---

# 煤矿冲击地压风险辅助研判大模型

本仓库提供一个基于 Qwen2.5-0.5B 微调并合并后的煤矿冲击地压风险辅助研判模型。模型面向煤矿采动应力监测与冲击地压防治场景，可根据现场背景、绝对应力、应力变化率、高位持续时间、埋深、顶底板条件等信息，输出结构化的危险等级、判断依据、防治建议和不确定性说明。

> 本项目仅用于学习、科研和辅助研判展示，不能替代煤矿现场专业人员的安全决策。

## 项目特点

- 基于 Qwen2.5-0.5B 基座模型进行垂直领域微调
- 使用 LoRA / SFT 方式训练煤矿冲击地压风险研判能力
- 已将 LoRA 权重与基座模型合并，可直接加载推理
- 输出格式更适合安全管理场景：危险等级、判断依据、防治建议、不确定性说明
- 适合用于 AI 产品作品展示、垂直大模型应用演示和煤矿安全辅助研判实验

## 文件结构

```text
.
├── README.md
└── qwen-0.5b-rock-burst-merged/
    ├── chat_template.jinja
    ├── config.json
    ├── generation_config.json
    ├── model.safetensors
    ├── tokenizer.json
    └── tokenizer_config.json
