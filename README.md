# LaTeX 中文简历模板（简洁清晰版）

本模板基于 Raj Shah 在 Overleaf 上发布的 **IIIT Vadodara Resume** 英文模板修改而来，旨在为中文求职者提供一份排版清晰、结构完整的简历模板。包含了教育背景、实习经历、项目经历、技能和自我评价等核心模块，并**支持照片插入**。

## 📌 致谢与原始版权

- **原始模板名称**：IIIT Vadodara Resume
- **原始作者**：Raj Shah
- **原始来源**：[Overleaf 模板库](https://www.overleaf.com/gallery/tagged/cv/page/2)
- **原始许可证**：[Creative Commons CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)

本修改版本在遵守 CC BY 4.0 许可证的前提下，对原始模板进行了以下修改：
- 将文档类从 `article` 更换为 `ctexart`，以支持中文编译
- 添加了 Font Awesome 6 图标支持
- 调整了页面布局和边距
- 新增了自定义命令（如 `\resumeProject`、`\resumePOR`）
- 将模块标题样式更换为 tcolorbox 灰色圆角块
- 修改了整体配色和字体设置
- 完善了自我评价等模块的示例内容

在此对原始作者 Raj Shah 表示感谢！

## ✨ 模板特点

- 使用 **XeLaTeX** 编译，完美支持中文（依赖 `ctex` 宏包）
- 页面布局紧凑，一页纸即可容纳丰富信息
- 内置 **Font Awesome 6** 图标，轻松添加电话、邮箱、地址、日历等小图标
- 自定义命令（如 `\resumeSubheading`、`\resumeProject`）让内容填写更简单、格式更统一
- 左侧姓名 + 右侧照片的头部设计，视觉均衡
- 模块标题使用浅灰色圆角色块，区分清晰
- 本修改版本许可证：**MIT**，可自由使用、修改和分发（同时需遵守原始 CC BY 4.0 署名要求）

## 📂 文件结构

- `my-resume.tex`：主文件，包含简历的所有内容和格式，你需要在这里填写个人信息。
- `iiitv.png`：示例照片，请替换为你自己的证件照（建议尺寸 2.3cm × 2.3cm）。
- `README.md`：本说明文件。

## 🛠️ 编译方法

1. **安装 LaTeX 发行版**  
   推荐安装 [TeX Live](https://tug.org/texlive/)（全平台）或 [MikTeX](https://miktex.org/)（Windows），确保包含 `ctex`、`fontspec`、`fontawesome6` 等常用宏包。

2. **选择编译器**  
   必须使用 **XeLaTeX**（因为模板使用了 `fontspec` 和系统字体）。  
   - 在 Overleaf 中，点击左上角“Menu”，将 Compiler 切换为 **XeLaTeX**。  
   - 在本地编辑器中（如 TeXstudio、VS Code），将编译命令设置为 `xelatex`。

3. **一键编译**（命令行示例）  
   ```bash
   xelatex my-resume.tex


🔧 如何自定义
修改个人信息
打开 LaTeX-code，找到以下部分并替换为你的真实信息：
\newcommand{\name}{姓名}
\newcommand{\phone}{12345678910}
\newcommand{\emaila}{xxxxxx@163.com}
\newcommand{\address}{地址}

替换照片
将 iiitv.png 换成你自己的照片（建议尺寸 2.3cm × 2.3cm，保持比例），并确保文件名一致。

调整模块内容
教育背景、实习经历、项目经历等均使用 \resumeSubheading 和 \resumeItemListStart...\resumeItemListEnd 结构，按示例填写即可。

工具技能和自我评价在文件末尾处修改。
