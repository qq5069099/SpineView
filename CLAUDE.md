# SpineView 发布约定

## 安装包来源

- 每个版本按渠道提供安装包，文件名 `<渠道>-SpineView-<版本>.zip`（例如 `windows-SpineView-1.5.9.zip`；渠道名以实际签发为准）。
- 安装包放在仓库根目录的 `github/` 文件夹（或仓库根目录）；`github/` 和 `*.zip` 已在 `.gitignore` 中忽略，不要提交。
- 发布时直接使用已有的 zip，不重新压缩、不改名。

## 发布步骤

1. 将各渠道 zip 放入 `github/`（或仓库根目录）。
2. 为每个 zip 生成同名 `.sha256`。
3. 创建/更新 `v<版本>` Release，把所有渠道的 zip 和 `.sha256` 作为独立资产上传；删除原有资产。
4. 更新发布说明，按渠道列出安装包和 SHA-256；README 指向 Releases，并提示按购买渠道选择。
5. 不要提交 zip、rar 或安装包文件夹。

## 说明

- GitHub 会自动附带 `Source code (zip)` 和 `Source code (tar.gz)`；仓库中没有商业源码，这两个归档可以保留，不需要移除。
