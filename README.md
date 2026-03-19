# Arxiv_Template

# 研究组论文标准模板


## 目录结构

- `main.tex`：主入口文件，Overleaf 的 Main file 设为它
- `references.bib`：参考文献库
- `template/`：模板类文件与主题配色
- `content/sec/`：正文各章节
- `content/resources/`：局部宏和额外包
- `content/figures/`：正文插图
- `content/tables/`：表格源码
- `assets/branding/`：学校、合作单位、课题组 Logo
- `assets/fonts/`：模板依赖字体

## 推荐使用方式

1. 把整个 `group_paper_template/` 目录复制为一篇新论文的工作目录。
2. 在 `main.tex` 中修改标题、作者、单位、通讯作者和页眉配置。
3. 在 `content/sec/` 中替换占位正文。
4. 在 `references.bib` 中维护参考文献。
5. 把正文图片放到 `content/figures/`，把品牌图放到 `assets/branding/`。

## Overleaf 设置

- Main file: `main.tex`
- Compiler: `XeLaTeX`
- Bibliography: `BibTeX`

推荐编译顺序：

1. `XeLaTeX`
2. `BibTeX`
3. `XeLaTeX`
4. `XeLaTeX`

如果 Overleaf 报大量 `Undefined control sequence`，优先检查编译器是不是误设成了 `pdfLaTeX`。

## 可改入口

主文件 `main.tex` 中最常改的是这些位置：

- `\documentclass[]{template/mac_automl_xmu_blue}`：切换模板主题
- `\setleftheadercontent{...}`：首页左上 Logo 组合
- `\setrightheadericon{...}`：首页右上项目图标
- `\setrunningheadericon{...}`：后续页页眉小图标
- `\setheadergroupname{...}`：后续页页眉组名
- `\title{...}`：论文标题
- `\setfrontauthors{...}`：作者
- `\setfrontaffiliations{...}`：单位
- `\setfrontcontact{...}`：通讯作者说明

## 主题文件

当前保留两个主题：

- `template/mac_automl_xmu_blue.cls`
- `template/mac_automl_jiageng_red.cls`

如果后面研究组要固定统一视觉，建议只保留一个主题，不要让每篇论文随意改色。

## 这份模板和原压缩包的关系

- 原始压缩包：保留，作为历史输入
- `mac_automl_template_src/`：原件解压副本
- `group_paper_template/`：整理后的研究组标准模板

这份模板默认不包含具体论文示例 PDF、`.bbl` 和历史实验图，避免新人直接在旧论文上改稿。
