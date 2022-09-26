# My configuration for LSP

This is mainly so I can port common configuration through a minimal `vimrc` easier.

## Installation

```vim
Plug 'prabirshrestha/vim-lsp'
Plug 'cherryramatisdev/cherrylsp.vim'
```

## Register lsp client

```vim
 if executable('typescript-language-server')
    au User lsp_setup call lsp#register_server({
          \ 'name': 'typescript-language-server',
          \ 'cmd': {server_info->['typescript-language-server', '--stdio']},
          \ 'allowlist': ['typescript', 'typescriptreact']
          \ })
  endif 
```
