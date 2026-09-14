# Chongqing Raffles City — v118
这是重庆来福士 Blender 可视化项目的非官方 v118 发布。项目输出属于视觉重建和展示用途，不是 BIM、测绘、竣工、官方数字孪生或工程授权资料。

## 下载内容

请下载 GitHub Release 中的五个正式 ZIP：

- 01_最终Blend_分卷1.zip
- 02_最终Blend_分卷2.zip
- 03_Assets素材_中文.zip
- 04_合并工具与验证说明_中文.zip
- 05_独立实时漫游Viewer_中文.zip

01、02、04 解压到同一父目录后，使用 04 中的 MERGE_BLEND.cmd 合并最终 Blend。05 是独立本地实时漫游 Viewer，不需要 Blender、Python、Node 或互联网。

## 校验值

SHA-256 请以 Release 中的 SHA256SUMS.txt 和仓库根目录同名文件为准。正式包均小于 100,000,000 bytes。

## 验证摘要

- 五个 ZIP：完整读取、路径和条目检查通过。
- 01 + 02 + 04：干净解压合并成功；合并 Blend 通过 Blender 5.2.1 LTS 无界面重开。
- 05：干净解压后本地服务和 Viewer 页面 HTTP 200；既有包内浏览器 QA 记录了模型、HDRI、预设和自由漫游控制。
- 宣传图：10 张 4K PNG 可读，仓库提供 10 张 1920×1080 JPEG 预览。

## 许可和免责声明

请阅读 THIRD_PARTY_NOTICES.md。原始项目内容归项目作者所有；第三方数据、软件和素材继续适用其原始许可。本发布不创建新的 LICENSE，也不推断商业、工程或品牌使用许可。
