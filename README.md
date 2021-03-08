# myvimrc 我的 vim 配置

### Reference

- 基于 [vim-go-tutorial](https://github.com/fatih/vim-go-tutorial)
- 基于 [vim.cpp](https://github.com/kingofctrl/vim.cpp)
- 参照 [vim-init](https://github.com/skywind3000/vim-init) 注释修改

### Featrue 特点

- 使用了 lsp 来替代 ale 动态语法检查，自动格式化
- 用 isort 自动排序 python 的 import
- [vim-go](https://github.com/fatih/vim-go) golang 优化体验
- [asyncomplete](https://github.com/prabirshrestha/asyncomplete.vim) 异步补全
- [ultisnips](https://github.com/SirVer/ultisnips)
- [vim-snippets](https://github.com/SirVer/honza/vim-snippets) 代码模板
- 自动补全括号等符号
- rg 查找替换多文件

+ [vim-polyglot](https://github.com/sheerun/vim-polyglot) 查看 markdown 效果

#### Editing

+ [delimitMate](https://github.com/Raimondi/delimitMate) 补全括号
+ [nerdcommenter](https://github.com/scrooloose/nerdcommenter) 自动注释
+ [vim-auto-save](https://github.com/907th/vim-auto-save) 自动保存
+ [vim-ripgrep](https://github.com/jremmen/vim-ripgrep) 搜索与替换多个文件

1. :Rg string
2. :cfdo %s/search/replace/gc


#### language server

+ [asyncomplete-lsp](https://github.com/prabirshrestha/asyncomplete-lsp.vim) 异步补全配置
+ [vim-lsp](https://github.com/prabirshrestha/vim-lsp) 语言服务
+ [vim-lsp-settings](https://github.com/mattn/vim-lsp-settings) 语言服务配置
+ [vim-isort](https://github.com/fisadev/vim-isort)  " sort python import

#### Navigation
+ [tagbar](https://github.com/majutsushi/tagbar)
+ [vim-fswitch](https://github.com/derekwyatt/vim-fswitch) { 'for': + ['c', 'cpp', 'objc'] }
+ [supertab](https://github.com/ervandew/supertab)

#### View

+ [gitgutter](https://github.com/airblade/vim-gitgutter) git 状态
+ [vim-airline](https://github.com/vim-airline/vim-airline)
+ [vim-airline-theme](https://github.com/vim-airline/vim-airline-themes) 状态条

### Prepare 准备

```sh
# 目的，用 ~/.vim/vimrc 作为入口文件，方便版本管理																
mv ~/.vimrc{,.bak} && mv ~/.vim{,.bak} # 移动 ~/.vimrc 与 ~/.vim
```

### Install 安装

```sh
git clone --depth=1 https://github.com/toyourheart163/.vim ~/.vim
```

#### 目录

平时修改 init 文件夹的文件即可

```
├── README.md
├── autoload/plug.vim # plug.vim 包管理工具
├── init  # 分开配置 basic keymaps plugins, Plug 包管理，可以更换 plug 放的位置
├── plugged # plug 的地方
└── vimrc # 入口配置
```

### 修改 vim-plug 管理插件所在的位置，避免重新下载

```vim
" ~/.vim/vimrc
let g:bundle_home = "~/.vim/plugged"
```
### Lsp 问题

- 可能与一些格式化插件冲突

### License

> GNU Free to use
