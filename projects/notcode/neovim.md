[The Only Video You Need to Get Started with Neovim](https://www.youtube.com/watch?v=m8C0Cq9Uv9o)

https://github.com/nvim-lua/kickstart.nvim#Install-Recipes

`06/08/25` Installed neovim and requirements for Kickstart using
`winget install --accept-source-agreements chocolatey.chocolatey`
`choco install -y neovim git ripgrep wget fd unzip gzip mingw make`
I think I'll do the Kickstart process another day when I'm more free, as I'm not sure if I'll be able to go back to the tutorial once I start.

***
`13/09/25` Started going about installing the Lazy plugin loader.

- Installed Lua 5.1, a dependency:
	- ```bash
	  curl -L -R -O https://www.lua.org/ftp/lua-5.1.tar.gz
	  tar zxf lua-5.1.tar.gz
	  cd lua-5.1
	  make linux test
```
- Some things seem broken, so I'm following [this tutorial](https://www.youtube.com/watch?v=6mxWayq-s9I) for now.
- config folder: `/home/sidharth/.config/nvim/`
- Enter default nvim file explorer: `nvim .`
- inside neovim: `:edit lua/sidharth/lazy.lua`
***
Decided to go with kickstart anyway.
- forked the kickstart repo
- cloned into config folder:
	- ```bash
	  git clone https://github.com/nvim-lua/kickstart.nvim.git "${XDG_CONFIG_HOME:-$HOME/.config}"/nvim
	  ```
***
![[Pasted image 20250913133748.png|400]]
***
Added these lines to `init.lua`:
```lua
vim.wo.relativenumber = true
vim.keymap.set('i', '<C-H>', '<C-W>', { desc = 'Delete previous word' })
```

***
`20/09/25` Installed the  `nvim-autopairs` plugin.
```lua
  {
    'windwp/nvim-autopairs',
    event = "InsertEnter",
    config = true
    -- use opts = {} for passing setup options
    -- this is equivalent to setup({}) function
  },
```
***
`28/10/25 `   `init.lua` location: `~/.config/nvim/`