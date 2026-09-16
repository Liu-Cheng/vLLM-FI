# vLLM-FI 论文源码

Overleaf 的主文档保持为 `main.tex`。各章节通过 `\input` 加载，不单独编译。

| 文件 | 内容 |
| --- | --- |
| `main.tex` | IEEE TCAD 导言区、标题、作者、章节加载顺序和参考文献配置 |
| `sections/abstract.tex` | 摘要和关键词 |
| `sections/introduction.tex` | 引言 |
| `sections/related-work.tex` | 相关工作 |
| `sections/framework.tex` | vLLM-FI 框架 |
| `sections/experimental-setup.tex` | 实验设置 |
| `sections/experimental-results.tex` | 实验结果 |
| `sections/conclusion.tex` | 结论 |
| `figures/architecture.tex` | Figure 1 图注与浮动体；在引言后提前加载，以排在第 3 页顶部 |
| `sample.bib` | 参考文献条目 |

## 协作编辑

- 编辑对应章节文件；只有修改公共宏包、作者信息或章节顺序时才需要编辑 `main.tex`。
- 每个正文章节文件包含自己的 `\section`，无需在主文件重复添加标题。
- 图片继续放在项目根目录；已有图片路径、引用键和标签保持不变。
- 同步 GitHub 前先协调其他编辑者保存修改；拆分可以减少不同章节之间的冲突，但同一章节同时修改仍可能冲突。
- 保留 `main.tex` 作为 Overleaf 主文档，不要通过删除主文件来解决同步冲突。

## 编译

从项目根目录执行 `latexmk -pdf main.tex`，或依次执行 `pdflatex main.tex`、`bibtex main`、两次 `pdflatex main.tex`。Overleaf 中使用 pdfLaTeX 编译 `main.tex`。
