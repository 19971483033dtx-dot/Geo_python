# Geo_python

Python + Streamlit 的地理空间数据处理与可视化项目（协作开发）。

[![CI](https://github.com/19971483033dtx-dot/Geo_python/actions/workflows/ci.yml/badge.svg)](https://github.com/19971483033dtx-dot/Geo_python/actions/workflows/ci.yml)
![License](https://img.shields.io/badge/license-MIT-blue)
![Python](https://img.shields.io/badge/python-3.10%2B-3776AB)

## 项目状态

> **起步阶段**：`app.py` 目前只是 Streamlit 入口骨架（导入 `streamlit` / `pandas` / `numpy`），业务功能待补充。

欢迎通过 Fork + Pull Request 一起完善，流程见 [CONTRIBUTING.md](CONTRIBUTING.md)。

## 环境要求

- Python 3.10 及以上
- 依赖见 [requirements.txt](requirements.txt)：`streamlit`、`pandas`、`numpy`

## 快速开始

```bash
git clone https://github.com/19971483033dtx-dot/Geo_python.git
cd Geo_python

# 建议使用虚拟环境
python -m venv .venv
# Windows (PowerShell)
.venv\Scripts\Activate.ps1
# macOS / Linux
source .venv/bin/activate

pip install -r requirements.txt
streamlit run app.py
```

启动后浏览器打开 <http://localhost:8501>。

## 目录结构

```
Geo_python/
├── app.py                     # Streamlit 应用入口
├── requirements.txt           # Python 依赖
├── README.md                  # 项目说明（本文件）
├── CONTRIBUTING.md            # 贡献指南
├── LICENSE                    # MIT 许可证
├── .gitignore                 # 忽略规则（含密钥文件）
└── .github/
    ├── workflows/ci.yml       # GitHub Actions：语法检查 + lint
    └── PULL_REQUEST_TEMPLATE.md
```

## 协作方式

本仓库是公开项目，**任何人都可以参与，不需要写权限**：

1. Fork 本仓库到自己的账号
2. 从 `main` 开分支（`feature/xxx`、`fix/xxx`）
3. 提交改动并在本仓库开 Pull Request
4. CI 通过 + 至少 1 位维护者 Approve 后合并

`main` 分支已开启保护：必须通过 PR 合并，且 CI（`test`）必须为绿。

详细规范（分支命名、提交信息、代码风格、安全红线）见 [CONTRIBUTING.md](CONTRIBUTING.md)。

## 反馈

- Bug / 需求：[Issues](https://github.com/19971483033dtx-dot/Geo_python/issues)
- 开放讨论：[Discussions](https://github.com/19971483033dtx-dot/Geo_python/discussions)

## 许可证

[MIT](LICENSE)