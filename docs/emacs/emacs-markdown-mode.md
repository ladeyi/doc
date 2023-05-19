# emacs-markdowm-mode 介绍

## 安装配置 ##

emacs 使用 `M-x` 输入 list-package, `C-s` 搜索 markdown-mode 进行安装.
预览 markdown, 需要安装额外工具 pandoc, `sudo apt install pandoc`.

在 emacs 的配置文件 `init.el` 中配置上：

``` lisp
(setq markdown-command "pandoc")
```

## 常用命令 ##

* Links and Images: `C-c C-l` and `C-c C-i`
* Text Styles: `C-c C-s`

`C-c C-s q` 设置引用块

`C-c C-s p` and `C-c C-s C` 设置代码块

* Headings: `C-c C-s`

`C-c C-s h` 根据上下文设置标题

> 如果在前面加 `C-u` 设置小一号标题, `C-u C-u` 设置大一号标题

`C-c C-s 1` - `C-c C-s 6` 设置一到六号标题

`C-c C-s ! C-c C-s @` 设置下划线标题, `C-c C-k` 撤销, `C-y` 重新把标题文本粘贴回去

* Horizontal Rules: `C-c C-s -`

> 如果在前面加 `C-u N`, 则可以选择插入的水平线的样式

* Footnotes: `C-c C-s f`

* Wiki Links: `C-c C-s w`

* Markdown and Maintenance Commands: C-c C-c

`C-c C-c m`: markdown-command > *markdown-output* buffer.

`C-c C-c p`: markdown-command > temporary file > browser.

`C-c C-c e`: markdown-command > basename.html.

`C-c C-c v`: markdown-command > basename.html > browser.

`C-c C-c w`: markdown-command > kill ring.

`C-c C-c o`: markdown-open-command.

`C-c C-c l`: markdown-live-preview-mode > *eww* buffer.

* Completion: `C-c C-]`

* table: `C-c C-s t`
