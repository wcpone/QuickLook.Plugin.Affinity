# QuickLook Plugin for Affinity files

为 Windows [QuickLook](https://github.com/QL-Win/QuickLook) 提供 Affinity 文档快速预览。这是轻量级预览器，不是 Affinity 文档渲染器。

## 支持的扩展名

- `.afphoto`
- `.afdesign`
- `.afpub`
- `.af`

扩展名匹配不区分大小写。

## 安装

1. 安装并启动 Windows QuickLook。
2. 从本仓库或 Release 下载 `QuickLook.Plugin.AffinityViewer.qlplugin`。其 SHA-256 见 `QuickLook.Plugin.AffinityViewer.qlplugin.sha256`。
3. 选中 `.qlplugin` 文件，按 <kbd>Space</kbd>，选择“安装”，然后重启 QuickLook。
4. 选中受支持的 Affinity 文件并按 <kbd>Space</kbd>。

供最终用户安装的是 `.qlplugin` 文件本身。历史文件 `QuickLook.Plugin.Affinity.zip` 含源码和构建产物，不是推荐的下载包。

## 当前限制

- 插件查找的是文件内嵌的 PNG，并不解析 Affinity 文档模型或渲染图层。
- 显示的宽高来自选中的内嵌 PNG，不一定是文档画布的真实尺寸。
- 内嵌图的选择使用启发式规则；如果存在更大的内嵌 PNG，可在预览中通过“`大`”按钮切换。
- 预览器会使用棋盘格画布显示透明像素，但最终观感仍取决于已安装的 QuickLook 版本和 Windows 主题。
- 加密、损坏、结构特殊或未来版本的 Affinity 文件，可能没有可用的内嵌 PNG。

## 反馈问题

请提供 Windows 版本、QuickLook 版本、文件扩展名、保存文件的 Affinity 应用及版本、文件大小，以及是否包含透明像素。请勿上传机密文件；优先提供最小复现样本。

## 开发

原始源码目前仍包含在历史 ZIP 中。后续会整理为干净的源码目录并补充可复现构建说明。项目目标框架为 .NET Framework 4.6.2，使用 WPF。

## 许可证

GPL-3.0。见 [LICENSE](LICENSE)。

