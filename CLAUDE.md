# SpineView 发布约定

- GitHub Releases 会自动附带 `Source code (zip)` 和 `Source code (tar.gz)`。这是 GitHub 的固定行为，无法关闭、隐藏或通过 API 删除；不要尝试移除。
- 对外下载入口必须直接指向安装包资产，不要引导用户打开 Release 页面。例如：
  - `https://github.com/qq5069099/SpineView/releases/download/v<版本>/SpineView-<版本>.zip`
  - `https://github.com/qq5069099/SpineView/releases/download/v<版本>/SpineView-<版本>.zip.sha256`
- 每次发版同步更新 README 中的直链。
- 每个 Release 必须上传安装包 zip 和对应的 `.sha256`。
- 如果确实需要完全没有源码归档的下载页，只能改用官网 / 对象存储等 GitHub Releases 之外的渠道。
