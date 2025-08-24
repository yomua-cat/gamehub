# 木然の摸鱼管理器（GameHub）

[![GitHub Stars](https://img.shields.io/github/stars/yomua-cat/gamehub?style=flat-square)](https://github.com/yomua-cat/gamehub/stargazers) [![GitHub Forks](https://img.shields.io/github/forks/yomua-cat/gamehub?style=flat-square)](https://github.com/yomua-cat/gamehub/network/members) [![GitHub issues](https://img.shields.io/github/issues/yomua-cat/gamehub?style=flat-square)](https://github.com/yomua-cat/gamehub/issues) [![GitHub tag (latest SemVer)](https://img.shields.io/github/v/tag/yomua-cat/gamehub?label=version&sort=semver&style=flat-square)](https://github.com/yomua-cat/gamehub/tags) [![Last Commit](https://img.shields.io/github/last-commit/yomua-cat/gamehub?style=flat-square)](https://github.com/yomua-cat/gamehub/commits) [![License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](LICENSE) [![CI](https://github.com/yomua-cat/gamehub/actions/workflows/ci.yml/badge.svg)](https://github.com/yomua-cat/gamehub/actions/workflows/ci.yml)

一个“开箱即用”的本地链接与资源管理器，单个 HTML 文件即可运行，支持文件夹/链接分组、搜索、拖拽移动、CSV 导入、HTML 一键导出和 GitHub 仓库同步，内置明暗主题切换与优雅的过渡动画。

> 代码入口：`木然の摸鱼管理器.html`（单文件应用）

---

## 目录
- [主要特性](#主要特性)
- [安装与启动](#安装与启动)
- [使用示例](#使用示例)
- [GitHub 仓库同步](#github-仓库同步)
- [配置与数据持久化](#配置与数据持久化)
- [贡献指南](#贡献指南)
- [许可证](#许可证)
- [致谢](#致谢)
- [补充说明](#补充说明)

---

## 主要特性
- 单文件应用：无需依赖与构建，现代浏览器直接打开即可使用。
- 分组管理：支持“新建文件夹 / 添加链接”，层级目录、面包屑导航与便捷操作。
- 智能搜索：实时搜索文件夹与链接，快速定位目标资源。
- 拖拽交互：链接可拖拽移动到任意文件夹，具备拖入高亮与动效反馈。
- 导入导出：
  - CSV 导入（带进度条与统计，支持同名更新与异常提示）
  - HTML 导出（自包含备份文件，双击即可还原使用）
- GitHub 同步：从指定仓库拉取文件清单，按扩展名/路径/大小过滤，写入目标文件夹并支持增量更新。
- 主题切换：明暗主题一键切换，动效顺滑；用户偏好持久化保存。
- 细节体验：悬停阴影、通知提示、无障碍焦点样式与移动端适配。

---

## 安装与启动
本项目无需安装依赖或构建流程，任选以下方式即可开始：

- 方法一：克隆仓库（推荐）
```bash
# 克隆仓库
git clone https://github.com/yomua-cat/gamehub.git
cd gamehub

# macOS 直接用浏览器打开（或双击文件）
open "木然の摸鱼管理器.html"
```

- 方法二：下载单文件
  1. 前往 Releases 页面下载最新版本的 `gamehub.html`
  2. 双击打开或拖入浏览器运行

---

## GitHub 仓库同步
- GitHub仓库同步功能正在重构,马上就好...
---

## 配置与数据持久化
- 数据存储
  - 页面内置“数据存储区”（HTML 中的隐藏区域）用于保存文件系统
  - 用户偏好（如主题、GitHub 同步配置、Token 等）使用浏览器 `localStorage`
- 主题偏好
  - 支持明暗主题切换，偏好会被记忆并在下次打开时自动应用
- 备份与迁移
  - 建议定期使用“导出 HTML”功能，将当前数据导出为自包含文件以备份

---

## 贡献指南
欢迎通过 Issue 和 Pull Request 贡献改进！在提交前，请确保：

- 工程规范
  - 为新增的函数与关键逻辑添加注释与必要的错误处理
  - 保持一致的代码风格（本项目为单文件 HTML + 原生 JS + Tailwind CSS CDN）

- 分支与提交信息
  - 分支命名：`feature/xxx`、`fix/xxx`、`chore/xxx`
  - 提交信息建议遵循 Conventional Commits：

```text
feat: 支持按扩展名过滤 GitHub 同步结果
fix: 修复 CSV 导入空行导致的解析异常
chore: 更新 README，补充使用说明
```

- 提交流程
  1. Fork 本仓库并创建特性分支
  2. 提交变更并发起 Pull Request（附带变更说明与截图）
  3. 等待评审与合并

---

## 许可证
本项目采用 MIT 许可证开源，详情见 [LICENSE](LICENSE)。

---

## 致谢
- 源代码: flysheep flysheep资源避难所
- UI 与样式：Tailwind CSS（CDN 方式）
- 图标：Font Awesome（CDN 方式）
- 徽章：Shields.io 提供的状态徽章服务

---

## 常见问题（FAQ）
- 打不开或空白页？
  - 请使用现代浏览器（Chrome/Edge/Firefox/Safari 最新版），并确保未被浏览器或安全软件拦截本地脚本执行
- 某些图标缺失或显示异常？
  - 已知uBlock Origin会屏蔽gamehub使用的图标,请在页面中关闭uBlock Origin
- 数据是否会丢失？
  - 主要数据保存在页面文件中，用户偏好存储在浏览器 `localStorage`；建议定期“导出 HTML”做离线备份
- 是否支持移动端？
  - 页面布局对常见移动端做了基础适配，建议横屏使用以获得更佳体验

---

## 补充说明
- 项目基于flysheep资源避难所-咩咩の摸鱼管理器开发,感谢flysheep提供的源代码
- 本项目不参与flysheep资源避难所的任何开发,也不参与flysheep资源避难所的任何功能更新
- 本项目不属于PunkHeart,也不与PunkHeart有任何关联
