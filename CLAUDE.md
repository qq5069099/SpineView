# SpineView 发布约定

## 分发方式

- 不使用 GitHub Releases：GitHub 会自动附带 `Source code (zip)` 和 `Source code (tar.gz)`，无法关闭或删除。
- 安装包以仓库根目录的 `SpineView-<版本>.rar` 分发，同时提交对应的 `.sha256`。
- 不要在仓库中保留安装包文件夹，只保留 rar。

## 发布步骤

1. 将 `SpineView-<版本>` 文件夹压缩为 `SpineView-<版本>.rar`。
2. 删除仓库中的 `SpineView-<版本>` 文件夹。
3. 生成 `SpineView-<版本>.rar.sha256`：
   `sha256sum SpineView-<版本>.rar > SpineView-<版本>.rar.sha256`
4. 更新 README 中的下载链接为仓库内 raw 直链：
   - `https://github.com/qq5069099/SpineView/raw/main/SpineView-<版本>.rar`
   - `https://github.com/qq5069099/SpineView/raw/main/SpineView-<版本>.rar.sha256`
5. 单独提交 rar 和 `.sha256`，提交信息必须带版本号，例如 `发布 SpineView 1.5.8 安装包`；不要与 README/CLAUDE 的通用改动混在同一个提交里。
6. 提交并推送；不要创建 GitHub Release。
7. 如果已经创建了对应 Release，删除它及其标签：
   `gh release delete v<版本> --repo qq5069099/SpineView --yes --cleanup-tag`
