# SpineView 发布约定

## 分发方式

- 使用 GitHub Releases 分发安装包。GitHub 会自动附带 `Source code (zip)` 和 `Source code (tar.gz)`；仓库中没有商业源码，这两个归档可以保留，不需要移除。
- 每个 Release 上传 `SpineView-<版本>.zip` 和 `SpineView-<版本>.zip.sha256`。
- 不要在仓库中保留 rar、zip 或安装包文件夹，安装包只放在 Release 资产中。
- README 下载入口指向 Releases 页面：`https://github.com/qq5069099/SpineView/releases`。

## 发布步骤

1. 将安装包目录压缩为 `SpineView-<版本>.zip`，并生成 `.sha256`。
2. 创建 `v<版本>` 标签和 GitHub Release，上传 zip 与 `.sha256`。
3. README 下载入口保持指向 Releases 页面；不要提交 zip、rar 或安装包文件夹到仓库。
