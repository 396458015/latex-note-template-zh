
# LaTeX Note Template (中文笔记模板)

📘 `latex-note-template-zh` 是一个基于 `book` 文类的 LaTeX 中文笔记模板，适用于撰写 **学术笔记**、**课程总结**、**公式推导**、**文献整理** 等结构化内容。模板默认支持章节（`chapter`）、目录、摘要、公式、图表、参考文献等内容，适合长期维护的学习与研究笔记写作。

> 🧪 本模板专为中文排版优化，兼容 XeLaTeX / LuaLaTeX 编译。

---

## 📌 功能特色

- ✅ 基于 `book` 类文档，支持多章结构
- ✅ 中文支持良好（适配 `ctex`）
- ✅ 支持中文目录、摘要、关键词等
- ✅ 自定义字体大小、标题格式
- ✅ 插入公式、图表、三线表、引用文献
- ✅ 参考文献支持 `bib` 文件，默认采用国标样式
- ✅ 结构清晰，便于持续维护与扩展

---

## 📁 项目结构

```
latex-note-template-zh/
├── main.tex                  # 主文件
├── setup/
│   └── format.tex            # 模板格式设置（字体、行距、标题等）
├── figures/                  # 图片目录（默认路径）
├── references/
│   ├── gbt7714-2005.bst      # 参考文献样式（国标）
│   └── Library.bib           # 参考文献数据库
└── output/                   # 输出目录（可选）
```

---

## 🚀 使用方法

### 1. 编译方式

推荐使用以下编译流程：

- `xelatex` → `bibtex` → `xelatex`*2

适用于 VS Code + LaTeX Workshop 插件，或本地终端。Overleaf 也可支持手动或自动编译。

### 2. 编译主文件

```bash
latexmk -xelatex main.tex
bibtex main
latexmk -xelatex main.tex
latexmk -xelatex main.tex
```

> 如果使用 LaTeX Workshop 插件，可在 `.vscode/settings.json` 中设置编译链。

---

## 📚 依赖宏包说明

以下为主要使用的宏包（自动安装）：

- `ctex`：中文支持
- `amsmath`, `amssymb`：数学公式
- `graphicx`, `subfigure`：插图支持
- `booktabs`, `tabularx`：美观表格
- `geometry`, `fancyhdr`：页面与页眉页脚设置
- `biblatex` / `bibtex`：参考文献管理

> 可根据需要自行扩展其他宏包。

---

## 🧱 使用建议

- 修改 `setup/format.tex` 自定义字体、字号、段落间距等格式
- 建议按章节拆分内容（如 `chapter1.tex`），使用 `\input` 引入
- 参考文献统一管理于 `references/Library.bib` 中

---

## 📄 License

本模板基于 MIT 协议开源，你可以自由使用、修改、分享。欢迎 PR 与 Issue！

---

## ✨ 致谢

本模板借鉴了多种中文 LaTeX 模板的设计思路，感谢社区资源的支持与启发。
