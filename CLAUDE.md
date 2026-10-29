# SpineView 发布约定

## 安装包来源

- 每个版本的安装包直接放在仓库根目录的 `github/` 文件夹中，文件名 `SpineView-<版本>.zip`（例如 `github/SpineView-1.5.9.zip`）。
- `github/` 已在 `.gitignore` 中忽略；不要把 zip、rar 或安装包文件夹提交到仓库。
- 发布时直接使用 `github/` 中的 zip，不重新压缩、不改名。

## 发布步骤

1. 将 `SpineView-<版本>.zip` 放入 `github/`。
2. 在 `github/` 中生成校验文件：
   `sha256sum SpineView-<版本>.zip > SpineView-<版本>.zip.sha256`
3. 创建 `v<版本>` 标签和 GitHub Release，上传 zip 与 `.sha256`。
4. 更新发布说明中的 SHA-256；README 下载入口保持指向 Releases 页面。
5. 不要提交 `github/`、zip、rar 或安装包文件夹。

## 说明

- GitHub 会自动附带 `Source code (zip)` 和 `Source code (tar.gz)`；仓库中没有商业源码，这两个归档可以保留，不需要移除。
