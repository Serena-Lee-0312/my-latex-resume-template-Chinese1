# LaTeX 中文简历模板 (简洁清晰版)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![LaTeX: XeLaTeX](https://img.shields.io/badge/LaTeX-XeLaTeX-blue.svg)](https://www.latex-project.org/)

本模板基于 Raj Shah 在 Overleaf 上发布的 **IIIT Vadodara Resume** 英文模板修改而来，旨在为中文求职者提供一份排版清晰、结构完整的简历模板。包含了教育背景、实习经历、项目经历、技能和自我评价等核心模块，并 **支持照片插入**。

---

## 📌 致谢与原始版权

- **原始模板名称**：[IIIT Vadodara Resume](https://www.overleaf.com/gallery/tagged/cv/page/2)
- **原始作者**：Raj Shah
- **原始来源**：Overleaf Gallery
- **原始许可证**：[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)

本修改版本在遵守 CC BY 4.0 许可证的前提下，对原始模板进行了以下改进：
- **中文化支持**：将文档类从 `article` 更换为 `ctexart`，原生支持中文。
- **图标增强**：添加了 **Font Awesome 6** 图标支持，简历更具现代感。
- **布局优化**：精调页面边距和行间距，提升阅读体验。
- **功能扩展**：新增自定义命令（如 `\resumeProject`、`\resumePOR`），内容填写更高效。
- **样式美化**：模块标题采用 `tcolorbox` 灰色圆角设计，区分度更高。
- **示例完善**：提供更加贴合国内求职习惯的模块划分和示例内容。

在此对原始作者 **Raj Shah** 表示衷心感谢！

---

## ✨ 模板特点

- 🚀 **编译高效**：使用 **XeLaTeX** 编译，完美支持中文（依赖 `ctex` 宏包）。
- 📄 **一页精简**：页面布局紧凑，适合将丰富信息浓缩在“一页纸”内。
- 🎨 **美观图标**：内置 Font Awesome 6，轻松添加电话、邮箱、地址、日历等。
- 🛠️ **易于维护**：封装了大量自定义命令，格式统一，修改方便。
- 🖼️ **图文均衡**：左侧个人信息 + 右侧证件照设计，视觉重心更平稳。
- 🔓 **开源自由**：本修改版本采用 **MIT** 许可证，可自由商用、修改。

---

## 📂 文件结构

| 文件名 | 说明 |
| :--- | :--- |
| `my-resume.tex` | **核心文件**。包含所有内容和格式，主要在此处填写信息。 |
| `iiitv.png` | **示例照片**。请替换为你自己的证件照（建议尺寸 2.3cm × 2.3cm）。 |
| `IIIT_Vadodara_Resume_Template.pdf` | **编译效果示例**。LaTeX 运行生成的 PDF，可预览最终简历排版。 |
| `README.md` | 项目说明文件。 |
---

## 🛠️ 编译方法

### 1. 推荐方式：Overleaf (云端免安装)

1. 登录 [Overleaf](https://www.overleaf.com/)，点击 **New Project** -> **Upload Project**，上传 ZIP 包。
2. **关键步骤**：点击左上角 **Menu**，在 **Compiler** 下拉菜单中选择 **XeLaTeX**。
3. 点击 **Recompile**，即可预览并下载 PDF。

### 2. 本地编译

如果你本地已有 LaTeX 环境：
- **发行版推荐**：安装 [TeX Live](https://tug.org/texlive/) (全平台) 或 [MiKTeX](https://miktex.org/) (Windows)。
- **编译命令**：
  ```bash
  xelatex my-resume.tex
  ```
- **编辑器**：推荐使用 VS Code (配合 LaTeX Workshop 插件) 或 TeXstudio。

---

## 🔧 如何自定义

### 修改个人信息
打开 `my-resume.tex`，找到头部定义的命令进行修改：

```latex
% ===== 请将以下信息替换为你的真实内容 =====
\newcommand{\name}{姓名}
\newcommand{\phone}{12345678910}
\newcommand{\emaila}{xxxxxx@163.com}
\newcommand{\address}{地址}
\newcommand{\github}{你的GitHub用户名}
% ===== 替换结束 =====
```

### 替换照片
将 `iiitv.png` 替换为你自己的照片，并保持文件名一致（或在 `.tex` 文件中修改路径）。建议尺寸为 **2.3cm × 2.3cm**。

### 模块调整
教育、实习、项目等模块均采用以下标准结构：
```latex
\resumeSubheading
  {单位名称}{地点}
  {职位/学位}{时间范围}
  \resumeItemListStart
    \item 描述你的具体成就或职责
    \item 使用关键词突出重点
  \resumeItemListEnd
```

---

## 📸 效果预览

![Resume Preview](IIIT_Vadodara_Resume_Template.pdf)
*(建议在上传后，将此处链接替换为你生成的简历截图)*

---

## ⚠️ 注意事项

1. **引擎选择**：必须使用 **XeLaTeX** 编译，否则中文和图标无法正常显示。
2. **字体说明**：
   - 默认使用 `SimHei` (黑体)。
   - **Overleaf 用户**：如果报错，请将 `\setCJKsansfont{SimHei}` 改为 `\setCJKsansfont{NotoSansCJKsc-Regular}`。
3. **页面边距**：如需微调，可修改 `geometry` 宏包的相关参数。

---

## 📄 许可证

本项目采用双重许可证：

1. **原始部分**：遵循 [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) 许可证，版权归 **Raj Shah** 所有。
2. **修改部分**：遵循 **MIT License**。

> **重要提示**：根据 CC BY 4.0 要求，即使您使用的是修改后的版本，也**必须**保留对原始作者 Raj Shah 的署名和来源引用。

---

Happy TeXing! 🌟 如果觉得好用，欢迎点个 **Star** 支持一下！
