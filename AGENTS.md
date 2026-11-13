# AGENTS.md

本文件面向 AI 编码代理（AI coding agents），用于说明本仓库的性质与结构。阅读本文件前不需要任何项目背景知识。

## 项目概述

这是 GitHub 用户 **宋子桓（SONG ZIHUAN，网名“代码小桓”）的个人资料页仓库**，即 GitHub 的特殊仓库 `SongZihuan/SongZihuan`（远程地址：`git@github.com:SongZihuan/SongZihuan.git`，默认分支 `main`）。该仓库的 `README.md` 会直接渲染在作者的 GitHub 个人主页上。

**本仓库不包含任何可执行的软件代码、库或应用程序。** 它没有源代码、没有依赖、没有构建产物，也不提供任何运行时行为。仓库的全部内容是个人主页文档。

## 技术栈与架构

- 无编程语言、无框架、无第三方依赖。
- 不存在 `pyproject.toml`、`package.json`、`Cargo.toml`、`Makefile`、`Dockerfile`、CI 工作流等任何构建或工程配置文件。如果将来出现此类文件，请更新本文件。
- 唯一的“运行时”是 GitHub 对 `README.md` 的 Markdown 渲染。README 使用内联 HTML `<picture>`，按 `prefers-color-scheme` 在深色与浅色之间切换两张静态 SVG 卡片（`dark_mode.svg`、`light_mode.svg`）。卡片是放在仓库根目录的静态文件，不引用外部统计图片，也不在本仓库内生成。卡片下方是一段中文简介和官网链接。

## 联系作者

- 主邮箱：`songzh0630@gmail.com`
- 网站：`https://song-zh.com`
