# Realtime Viewer Guide
本说明对应 GitHub Release v118 的 05_独立实时漫游Viewer_中文.zip。请完整解压，不要把 HTML、GLB 或 HDRI 单独拎出来运行。

## Start

1. 解压整个 05 号 ZIP。
2. 双击根目录中的 <code>打开实时漫游Viewer.cmd</code>。
3. 等待浏览器打开本机地址；服务只监听 127.0.0.1。
4. 如果端口 58446 已被占用，启动器会继续尝试后续端口。

本包不依赖 Blender、Python、Node 或互联网。浏览器需要支持 WebGL2，并且允许访问本机 loopback。

## Controls

默认状态是观察模式：

- 鼠标拖拽旋转相机，滚轮缩放。
- 点击 HERO、RIVER、CITY、CRYSTAL、PODIUM、LOW、HIGH、PODIUM_CLOSE 切换预设。
- 点击“进入自由漫游”进入自由模式。

自由模式：

- W / A / S / D：前进、左移、后退、右移。
- Q / E：下降、上升。
- Shift：加速。
- 速度选择：6、18、45、100 m/s。
- Home：回到 Hero。
- “重置视角”：恢复当前预设。
- Esc：退出浏览器 pointer lock；再次点击进入按钮可重新进入。
- “全屏”：切换浏览器全屏。

浏览器拒绝 pointer lock 时，Viewer 会保留鼠标左键拖拽观察的回退路径。

## Stop

关闭浏览器标签页不会必然停止隐藏的 PowerShell 服务。本包没有独立停止脚本。需要停止时，在任务管理器中结束命令行包含 <code>server\portable_server.ps1</code>、且位于 Viewer 解压目录的对应 <code>powershell.exe</code>。不要结束不相关的 PowerShell 进程。

## Troubleshooting

- 页面没有模型：确认 ZIP 是完整解压，且 <code>exports\viewer\v118r3</code>、<code>viewer\vendor</code> 与 <code>viewer\assets</code> 都仍在原位置。
- 页面打不开：重新双击启动器；若端口已占用，启动器会自动换端口。
- 画面很慢：关闭其他 WebGL 页面，降低浏览器缩放或使用更强的独立 GPU。
- 双击没有窗口：确认 Windows PowerShell 可执行，并在文件属性中解除来自互联网的阻止标记（如果系统显示该选项）。

## English Summary

Extract the complete package 05 and double-click <code>打开实时漫游Viewer.cmd</code>. It launches a local 127.0.0.1 service and opens the default browser. It does not require Blender, Python, Node, or internet access.

Orbit with mouse drag and zoom with the wheel. Use the eight presets HERO, RIVER, CITY, CRYSTAL, PODIUM, LOW, HIGH, and PODIUM_CLOSE. Click “进入自由漫游” to enter free mode. W/A/S/D move, Q/E change elevation, Shift boosts, the speed selector offers 6/18/45/100 m/s, Home returns to Hero, Esc exits pointer lock, and the fullscreen button toggles fullscreen. If pointer lock is unavailable, hold the left mouse button to look around.
