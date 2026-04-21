# 技术决策

## 方案选择：GitHub 数据驱动
- 将任务数据抽离为独立的 `data/tasks.json` 文件
- HTML 页面通过 `fetch` API 从同仓库加载 JSON 数据
- 用户更新 JSON 文件并 push，GitHub Pages 自动重新部署
- 看板页面每次打开时从仓库获取最新数据

## 数据格式设计
- 保持与原始 HTML 中的 `cards` 数组结构兼容
- 添加 `meta` 字段包含更新时间等信息
- 支持人员和项目的配置化

## 优势
- 零成本（GitHub Pages 免费）
- 无需后端服务器
- 用户只需修改 JSON 文件即可更新
- 支持 Git 版本管理，可追溯历史
