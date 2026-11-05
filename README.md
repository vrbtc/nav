# nav — 项目导航页

所有已部署站点与后台入口的统一门户：**https://vrbtc.github.io/nav/**

## 架构

- `index.html` — 渲染逻辑（纯静态，零依赖，不支持修改）
- `projects.json` — **唯一数据源**，所有入口都在这里维护

## 新项目接入（一句话）

在 `projects.json` 对应分组的 `items` 里添加一条记录：

```json
{
  "name": "项目名称",
  "desc": "一句话描述",
  "url": "https://访问地址",
  "repo": "https://github.com/vrbtc/仓库名",
  "tag": "GitHub Pages"
}
```

保存推送后页面自动生效，无需改 `index.html`。

> 注意：本仓库为公开仓库（GitHub Pages 免费版限制），**不要**在 `projects.json` 中写入密码、Token 等敏感信息。
