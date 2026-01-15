---
layout: "default"
title: "🎓 PaperMate - Your AI Academic Paper Assistant"
description: "📄 Analyze and translate academic papers effortlessly with PaperMate, your AI assistant for deep insights and seamless comprehension."
---
# 🎓 PaperMate - Your AI Academic Paper Assistant

[![Download PaperMate](https://img.shields.io/badge/Download-PaperMate-brightgreen)](https://github.com/memecrypto/PaperMate/releases)

PaperMate 是 AI 学术论文分析助手，支持论文解析、翻译、术语记忆与自适应对话。

![PaperMate](./image.png)

## ✨ 功能简介

### 1. 📄 论文解析与翻译（保留格式）

- 论文解析为 Markdown 后进行翻译，结构与公式不丢失。
- 中英对照阅读界面。
- 翻译采用 ReAct Agent 架构，结合 arXiv 与网络检索，补充背景、动机与切入点。
- 输出强相关论文链接，并给出相关性说明。
- 深度解析核心创新点：是什么、为什么重要、与已有方法对比、关键模块细节。
- 给出实验结果、优势与局限性。
- 提供 AI 推断的可行未来方向。

### 2. 💡 术语记忆与全局高亮

- 划词触发 AI 解析专业术语。
- 解析后在项目内全局高亮。
- 鼠标悬停显示术语解释与上下文。

### 3. 💬 用户画像驱动的论文对话

- 对话中自动更新用户画像。
- AI 根据画像实时调整回答深度与表达方式。

## 🚀 快速开始

### 🔥 方式一：Docker 一键启动（推荐）

**使用 Docker 数据库**：
```bash
cp backend/.env.example backend/.env
# 编辑 backend/.env，DATABASE_URL 配置为：
# DATABASE_URL=postgresql+asyncpg://postgres:postgres@db:5432/papermate

docker-compose --profile db --profile dev up -d
```

**使用外部数据库**：
```bash
cp backend/.env.example backend/.env
# 编辑 backend/.env，DATABASE_URL 配置为你的数据库地址

docker-compose --profile dev up -d
```

访问：
- 前端：[http://localhost:5173](http://localhost:5173)
- 后端 API：[http://localhost:8000/docs](http://localhost:8000/docs)

**首次使用**：
1. 访问前端 [http://localhost:5173](http://localhost:5173)
2. 点击注册，创建第一个用户（自动成为管理员）。
3. 注册后，其他用户无法自行注册，需要管理员添加。

### 🖥️ 方式二：本地开发启动

**前置条件**：
- Python 3.7 或更高版本
- 安装依赖库：可以使用以下命令安装依赖：
```bash
pip install -r requirements.txt
```

**步骤**：
1. 从 [PaperMate Releases](https://github.com/memecrypto/PaperMate/releases) 页面下载程序包。
2. 解压下载的文件。
3. 在终端中，导航到解压文件夹并运行以下命令：
```bash
python main.py
```

访问：
- 前端：[http://localhost:5173](http://localhost:5173)
- 后端 API：[http://localhost:8000/docs](http://localhost:8000/docs)

通过以上步骤，你可以顺利启动 PaperMate 并享受其强大的功能。