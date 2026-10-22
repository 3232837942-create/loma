# 罗马纪年 · ROMA ATLAS

前27年至395年的可玩历史地图：12个地图阶段、12座城市、26个事件、8位人物。搜索、图层、地图缩放拖动、人物节点和城市名称随年代联动。

## 本地运行

需要Node.js 24。`npm ci` 后运行 `npm run build`、`npm start`。默认3000端口；可通过PORT或`--port`更改。

构建同时生成`artifacts/roma-atlas.html`独立文件，内嵌全部地图、样式与交互。当前托管浏览器禁止file导航，因此采用内嵌文档方式验证，不声称验证了直接file导航。

`npm test`运行数据检查；服务启动后`npm run test:browser`运行Chromium交互检查。TEST_URL可设为带前缀的URL，CHROMIUM_PATH可覆盖系统浏览器。

## 网页发布

工作区路径不是公开网址，运行中的进程也不会随新云环境恢复。本项目准备了GitHub Pages工作流，但没有因为写入此文件就自动发布。只有用户授权推送、仓库配置Pages来源为GitHub Actions并且部署成功后，才能提供实际可访问的网址。

## 数据与恢复边界

此前云环境已不可用，新环境仓库为空。本版依据会话记录重建应用，并重新取得Natural Earth陆地数据；此前research原始证据库尚未完整恢复，不将其列为当前已持有文件。

地理底图来自[natural-earth-vector](https://github.com/nvkelso/natural-earth-vector/blob/master/geojson/ne_50m_land.geojson)，为公共领域。城市标识关联Pleiades。所有领土与交通联系为编辑示意，非已完成学术审校的历史GIS；现代书目的具体页码与若干事件卷章仍待核。来源卡明确记录核验程度。
