## 这个 PR 做了什么

<!-- 一两句话说明改动内容 -->

## 为什么需要

<!-- 关联 Issue：Closes #123 -->

## 如何验证

<!-- 本地运行方式 / 测试步骤 / 截图 -->

## 自检清单

- [ ] 目标分支是 `main`，改动聚焦在单一主题
- [ ] 已与最新 `main` 同步（rebase），无冲突
- [ ] 本地通过 `python -m py_compile app.py` 与 `ruff check --select E9,F63,F7,F82 .`
- [ ] 新增/修改的依赖已写入 `requirements.txt`
- [ ] 未提交任何密钥、`.env`、`.streamlit/secrets.toml`