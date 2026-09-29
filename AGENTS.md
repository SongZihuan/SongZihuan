# AGENTS.md

本文件面向 AI 编码代理（AI coding agents），用于说明本仓库的性质与结构。阅读本文件前不需要任何项目背景知识。

## 项目概述

这是 GitHub 用户 **宋子桓（SONG ZIHUAN，网名“写代码的小桓Huan”）的个人资料页仓库**，即 GitHub 的特殊仓库 `SongZihuan/SongZihuan`（远程地址：`git@github.com:SongZihuan/SongZihuan.git`，默认分支 `main`）。该仓库的 `README.md` 会直接渲染在作者的 GitHub 个人主页上。

**本仓库不包含任何可执行的软件代码、库或应用程序。** 它没有源代码、没有依赖、没有构建产物，也不提供任何运行时行为。仓库的全部内容是个人主页文档。

## 技术栈与架构

- 无编程语言、无框架、无第三方依赖。
- 不存在 `pyproject.toml`、`package.json`、`Cargo.toml`、`Makefile`、`Dockerfile`、CI 工作流等任何构建或工程配置文件。如果将来出现此类文件，请更新本文件。
- 唯一的“运行时”是 GitHub 对 `README.md` 的 Markdown 渲染。内容使用左对齐标题、段落、列表和链接，不依赖内联 HTML、外部统计图片或自动生成卡片。

## 仓库结构

| 文件 | 语言 | 作用 |
| --- | --- | --- |
| `README.md` | 中文为主 | GitHub 个人主页内容：简短技术定位、编程语言与解释器路线、工程工具与基础设施、源码阅读入口、早期探索与归档状态、联系方式和开源约定 |
| `LICENSE` | 英文 | MIT License，Copyright (c) 2026 SONG ZIHUAN |
| `.gitignore` | — | Git 忽略规则 |

个人介绍、经历与文章由个人官网承担；本仓库聚焦代码项目、具体机制与源码阅读入口。

治理性文档（许可证介绍、安全策略、行为准则、法律相关声明）由个人官网承担，仓库内不再保留对应文件。README 页尾集中链接到官网：

- 开源策略总页：`https://song-zh.com/opensource`
- 安全策略：`https://song-zh.com/opensource/security-policy`
- 行为准则：`https://song-zh.com/opensource/code-of-conduct`
- 联系页：`https://song-zh.com/contact`
- 个人官网与博客：`https://song-zh.com`

无子目录、无测试、无脚本。

## 安全与法律注意事项

- 安全漏洞报告**不得**通过公开 issue 或 PR 提交，应遵循博客上的安全策略（`https://song-zh.com/opensource/security-policy`）通过邮件报告。
- 项目默认以 MIT License 发布（见 `LICENSE` 文件，介绍见 `https://song-zh.com/opensource/mit-license`）。
- 贡献者须遵守博客上的行为准则（`https://song-zh.com/opensource/code-of-conduct`）。
- 仓库中不含任何密钥或敏感凭据；请勿在文档中新增真实私钥、密码等敏感信息。

## 联系作者

- 主邮箱：`work@song-zh.com`
- 联系页：`https://song-zh.com/contact`
