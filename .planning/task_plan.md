# 任务计划：GitHub 自动化数据驱动看板

## 需求
用户希望看板能通过 JSON 数据文件自动更新，流程：
1. 用户更新 `data/tasks.json` 文件并推送到 GitHub 仓库
2. 看板页面自动从仓库中读取最新数据并渲染
3. GitHub Pages 自动部署更新后的内容

## Phase 1: 数据分离 - `complete`
- [x] 从 `work-board.html` 中提取任务数据到 `data/tasks.json`
- [x] 修改 `work-board.html` 通过 `fetch` 加载 JSON 数据
- [x] 修改 `work-board-enhanced.html` 同样支持外部数据加载
- [x] 本地测试两个页面都能正确读取 JSON 数据

## Phase 2: 添加首页入口 - `complete`
- [x] 创建 `index.html` 作为入口页面，提供两个版本的链接
- [x] 页面包含简单说明和使用指南

## Phase 3: 推送更新到 GitHub - `complete`
- [x] 将所有修改推送到 GitHub 仓库
- [x] 验证 GitHub Pages 自动部署

## Phase 4: 提供使用说明 - `complete`
- [x] 告诉用户如何更新 `data/tasks.json`
- [x] 说明更新数据后推送即可自动更新看板
