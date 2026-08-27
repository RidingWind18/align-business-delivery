# Source And Release Relationship

本仓库是 `align-business-delivery` Skill 的公开安装与反馈入口。

Skill 的完整实验、真实项目复盘和版本决策在维护者的私有演进仓库 `ai-delivery-playbook` 中完成。公开仓库不是私有仓库的完整镜像，只接收经过脱敏审查、适合公开使用的 Skill 文件和说明材料。

两个仓库采用以下版本关系：

- 使用相同的语义化版本号和 tag 名称。
- Git commit hash 可以不同，因为公开仓库排除了私有材料。
- 私有实验变化不自动形成公开版本。
- Skill 行为变化发布后，公开仓库与私有源使用相同版本号。

公开使用者只需跟踪本仓库的 tag、GitHub Release 和 `CHANGELOG.md`，不依赖访问私有演进源。
