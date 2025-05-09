---
title: "LM Studio 本地部署大模型的详细操作教程及硬件要求"
description: "LM Studio 是一款强大的客户端应用，支持本地离线运行各类开源大语言模型（LLMs）。通过LM Studio工具实现各类型AI模型本地部署的操作方法方式。"
date: 2024-03-15T14:42:22+08:00
Lastmod: 2025-03-28
draft: false
description: ""
showComments: true
featureimage: "https://picsum.photos/seed/2128c8f0/1600/900.webp"
tags: ["技术教程","经验转载","大模型部署"]
## externalUrl: https://linux.do/t/topic/310934
series: "大模型本地部署"
series_order: 1
---

## 🌟 LM Studio 介绍

LM Studio 是一款强大的客户端应用，支持本地离线运行各类开源大语言模型（LLMs）。通过 [LM Studio](https://lmstudio.ai/) 工具，可以快速实现各类大语言模型的本地部署，无需依赖网络，独立运行，保障数据安全。本文将详细介绍 LM Studio 的使用方法及硬件要求，帮助轻松上手本地大模型部署。

**核心特点：**

- ✅ **本地运行**：完全离线，不依赖网络。
- ✅ **数据安全**：独立环境，保障隐私。
- ✅ **高效流畅**：快速加载，实时响应。

**硬件推荐要求：**

- 🖥️ **GPU**：GTX 3060TI 及以上，显存 8GB 以上。
- 💻 **CPU**：频率 3.3GHz 及以上。
- 💾 **硬盘**：250GB 及以上可用空间。

{{< alert >}}
**注意：**
LM Studio 并非开源软件，但官方承诺不会收集敏感数据。部分遥测配置仅用于程序优化和故障排除。
硬件要求为推荐指标，若低于给出的配置，功能运行可能不正常，体验大大下降！
{{< /alert >}}

---

## 🛠️ 安装教程（Windows）

### 步骤一：下载 LM Studio

1. 访问 [LM Studio 官网](https://lmstudio.ai/)，点击下载按钮。
![下载按钮](download_lm.png)

### 步骤二：安装 LM Studio

1. 双击下载的安装包，按照提示完成安装。
2. 安装完成后，桌面将显示 LM Studio 图标。
<!-- ![LM Studio 图标](img/llm/lm_icon.png) -->

---

## 🚀 通过 LM Studio 安装并本地运行大模型

### 步骤一：启动 LM Studio

1. 双击桌面图标，启动 LM Studio。
2. 默认界面会显示推荐的模型，可以选择跳过直接进入下一步。
![LM Studio 主界面](img/llm/desktop.png)

### 步骤二：搜索并下载 DeepSeek 模型

1. 点击顶部菜单栏的“选择模型”按钮。
2. 在搜索框中输入大模型名称如“DeepSeek”，点击“Search More”查看更多结果。
3. 选择适合的模型版本，点击下载。

### 步骤三：加载并运行模型

1. 下载完成后，返回主界面，选择已下载的 DeepSeek 模型。
2. 根据电脑性能调整配置参数，点击“Load Model”加载模型。
3. 在聊天界面中，输入问题即可获得模型回复。
![load_llm](img/llm/load_llm.png)

---

## ❓ 常见问题

### ~~问题：模型界面无法搜索或者显示~~(当前问题已经解决，官方自动使用镜像站点)

~~**原因**：相关网站被屏蔽，无法访问。~~

~~**解决方法**：~~

1. 第一种：绕过屏蔽，不用多说。
2. 第二种：修改软件内配置文件（**不推荐**，每次更新都需要重新来一次）。具体步骤为：右键打开应用文件所在位置，依次进入目录 `app-0.3.5\resources\app\.webpack`，通过vs-code 打开该目录，搜索替换
`huggingface.co`为`hf-mirror.com`，保存重新打开LM。
1. 第三种：使用下载好的离线模型（**推荐**）。直接从国内的镜像站点搜索下载“模型名称-GGUF”，下载好相应的文件，放置到LM本地目录当中刷新即可。

### 问题：提示无意义的英文消息

**原因**：模型加载失败或配置不足。

**解决方法**：检查硬件配置，重新加载模型。

### 问题：模型未成功预加载

**原因**：电脑性能不足。

**解决方法**：尝试更换更高配置的电脑。

---

## 🎉 结语

通过 LM Studio，可以轻松实现大语言模型的本地部署，享受高效、安全的 AI 对话体验。
