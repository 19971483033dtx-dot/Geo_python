# 贡献指南

感谢参与 `Geo_python`！本仓库是公开项目，任何人均可通过 **Fork → Pull Request** 参与，无需仓库写权限。

## 1. 开发流程

```bash
# 1) Fork 后在本地克隆你自己的 fork
git clone https://github.com/<你的用户名>/Geo_python.git
cd Geo_python

# 2) 加上游仓库，便于同步
git remote add upstream https://github.com/19971483033dtx-dot/Geo_python.git

# 3) 从最新的 main 开分支
git fetch upstream
git checkout -b feature/你的功能名 upstream/main

# 4) 修改、提交、推送
git add -A
git commit -m "feat: 描述你的改动"
git push -u origin feature/你的功能名
```

然后在 GitHub 上点 **Compare & pull request**，目标分支选 `main`。

## 2. 分支命名

| 前缀 | 用途 | 示例 |
| --- | --- | --- |
| `feature/` | 新功能 | `feature/upload-shp` |
| `fix/` | 修 bug | `fix/readme-typo` |
| `docs/` | 文档 | `docs/api-notes` |
| `chore/` | 构建、依赖、配置 | `chore/bump-pandas` |

## 3. 提交信息

采用 Conventional Commits：

```
<type>(optional scope): <subject>

feat: 增加数据上传组件
fix: 修复空表导致崩溃
docs: 补充运行说明
```

## 4. Pull Request 要求

- [ ] 目标分支是 `main`，PR 尽量小而聚焦（一个 PR 只做一件事）
- [ ] CI（GitHub Actions）必须通过
- [ ] 至少 1 位维护者 Approve
- [ ] 描述里写清：做了什么、为什么、如何验证
- [ ] 与最新 `main` 同步，冲突已解决

同步上游并解决冲突：

```bash
git fetch upstream
git rebase upstream/main
# 解决冲突后
git add <冲突文件>
git rebase --continue
git push --force-with-lease
```

## 5. 代码风格

- Python 3.10+，遵循 PEP 8
- 提交前本地自检（CI 会跑同样的检查）：

```bash
python -m py_compile app.py
ruff check --select E9,F63,F7,F82 .
```

- 新增依赖请写入 `requirements.txt`，并在 PR 描述里说明原因。

## 6. 安全红线

仓库是**公开**的，禁止提交：

- 任何 token、API Key、密码、数据库连接串
- `.streamlit/secrets.toml`、`.env`（已在 `.gitignore` 中忽略）
- 未脱敏的业务数据 / 个人信息

如果不小心提交了密钥：立刻在对应平台**吊销**，并联系维护者清理历史。

## 7. 问题与讨论

- 有 bug 或需求：开 [Issue](https://github.com/19971483033dtx-dot/Geo_python/issues)
- 开放式讨论：用 [Discussions](https://github.com/19971483033dtx-dot/Geo_python/discussions)