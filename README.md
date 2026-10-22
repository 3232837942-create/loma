# 罗马纪年 · ROMA ATLAS

前27年至395年的可玩历史地图：12个地图阶段、12座城市、26个事件、8位人物。搜索、图层、地图缩放拖动、人物节点和城市名称随年代联动。

## 本地运行

需要Node.js 24。`npm ci` 后运行 `npm run build`、`npm start`。默认3000端口；可通过PORT或`--port`更改。

构建同时生成`artifacts/roma-atlas.html`独立文件，内嵌全部地图、样式与交互。当前托管浏览器禁止file导航，因此采用内嵌文档方式验证，不声称验证了直接file导航。

`npm test`运行数据检查；服务启动后`npm run test:browser`运行Chromium交互检查。TEST_URL可设为带前缀的URL，CHROMIUM_PATH可覆盖系统浏览器。

## 网页发布

工作区路径不是公开网址，运行中的进程也不会随新云环境恢复。用户已授权推送和公开发布；源代码已推送main，构建产物准备发布到gh-pages分支。

首次启用时，在仓库Settings → Pages中选择“Deploy from a branch”，分支选择gh-pages，目录选择/(root)，保存。当前环境对GitHub管理API的访问被网络代理拒绝，不能自动完成这个设置。只有站点部署成功并能实际请求后，才能声称公网已可访问。

另保留可手动触发的Actions部署工作流；该方式需要Pages来源配置为GitHub Actions。默认不在每次源码推送时触发，避免未启用Pages造成反复失败。

## 数据与恢复边界

此前云环境已不可用，新环境仓库为空。本版依据会话记录重建应用，并重新取得Natural Earth陆地数据；此前research原始证据库尚未完整恢复，不将其列为当前已持有文件。

地理底图来自[natural-earth-vector](https://github.com/nvkelso/natural-earth-vector/blob/master/geojson/ne_50m_land.geojson)，为公共领域。城市标识关联Pleiades。所有领土与交通联系为编辑示意，非已完成学术审校的历史GIS；现代书目的具体页码与若干事件卷章仍待核。来源卡明确记录核验程度。
