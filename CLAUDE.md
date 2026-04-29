# 开发约定

## 命令参考文档

`skills/devicemanager/references/commands/` 目录由 `devicemanager-cli` 仓库的 `make docs` (cmd/docgen) 自动生成，**请勿手动编辑**。

如需更新：

1. 在 `devicemanager-cli` 仓库执行 `make docs`
2. 将生成的 markdown 文件复制到本仓库 `skills/devicemanager/references/commands/` 目录

## 发版流程

1. 更新 `.claude-plugin/plugin.json` 中的 `version`
2. 更新 `CHANGELOG.md`
3. 提交并打 tag（格式 `v0.x.0`）
