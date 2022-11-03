# Check Config
if listing does not return .config, mkdir .config
```bash
> ls -la 
> mkdir .config
❯ cd .config
❯ mkdir nvim
❯ cd nvim
> nvim init.vim
```

we start with `:set number` enabling row numbering, `:setrelativenumber` for showing the relative number of the line we are currently . further more we have additional 

- :set number
- :set relativenumber
- :set autoindent
- :set tabstop=4
- :set shiftwidth=4
- :set smarttab
- :set softtabstop=4
- :set mouse=a to enable 

plug in  Vimplug manager from[ junegunn repos]([junegunn/vim-plug: Minimalist Vim Plugin Manager (github.com)](https://github.com/junegunn/vim-plug))

```bash
>curl -fLo ~/.var/app/io.neovim.nvim/data/nvim/site/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

adding plug setup
```vi
call plug#begin()

Plug 'http://github.com/tpope/vim-surround' " Surrounding ysw)
Plug 'https://github.com/preservim/nerdtree' " NerdTree
Plug 'https://github.com/tpope/vim-commentary' " For Commenting gcc & gc
Plug 'https://github.com/vim-airline/vim-airline' " Status bar
Plug 'https://github.com/lifepillar/pgsql.vim' " PSQL Pluging needs :SQLSetType pgsql.vim
Plug 'https://github.com/ap/vim-css-color' " CSS Color Preview
Plug 'https://github.com/rafi/awesome-vim-colorschemes' " Retro Scheme
Plug 'https://github.com/neoclide/coc.nvim'  " Auto Completion
Plug 'https://github.com/ryanoasis/vim-devicons' " Developer Icons
Plug 'https://github.com/tc50cal/vim-terminal' " Vim Terminal
Plug 'https://github.com/preservim/tagbar' " Tagbar for code navigation
Plug 'https://github.com/terryma/vim-multiple-cursors' " CTRL + N for multiple cursors

set encoding=UTF-8

call plug#end()
```

the `plugged` directory will be in .local/share/nvim
remember this is important So, the information it gives us is that in the end **the plug.vim file must (or should, dunno) end up in the** _**autoload**- folder.

One of the easiest ways, to locate it [(jdaho's post)](https://www.reddit.com/r/neovim/comments/ehlmuf/fix_installing_vimplug_e117_unknow_function/fck730b?utm_source=share&utm_medium=web2x) is to open neovim and type `:echo stdpath('config')`It will give you a path to use into the curl command
```bash
curl -fLo [path_to_use]\autoload\plug.vim --create-dirs https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```
