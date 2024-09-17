# Keyboard Shortcuts

- How to move to move to next zsh tab or previous zsh tab:
	- `control + tab or control + shift + tab`


<br>

# FZF Plugin

- To use the fzf completions (ls /**) press tab not enter!
	- $ `ls /**`
- [Documentation on the FZF plugin.](https://github.com/junegunn/fzf)

<br>

# Consider adding plugins to enhance the Vi mode for zsh:
- [Link to vim plugins.](https://github.com/zsh-vi-more/)
- [Sample ZSH config file.](https://gitlab.com/xPMo/dotfiles.cli/-/blob/dots/.config/zsh/local/zle.zsh)

<br>

# Zsh Completion Shell Scripting
- If you want to have multiple "items" for one description in a single action you have to add the items as separate actions... so when it gets passed to the completions function it will automatically get put on the same line.
    - **Example:**

`testarray=("Item 1:Item 1 & Item 2 share the same description", "Item 2:Item 1 & Item 2 share the same description", "Item 3:Description for Item 3", "Item 4:Description for Item 4")`

`describe 'Arguments' testarray`

<br>

- ***Disable sorting in completion helpers***
    - The _arguments compsys utility function has the `-O` option which ***allows you to pass an array*** of common options to subsequent `compadd` calls:
        - `local -a copts=( -o nosort ); _arguments -O copts ...`
    - For _describe you can pass options after completions:
        - `_describe ... -o nosort`




<br>

# Documentation
- [List of Zsh Keybindings.](https://zsh.sourceforge.io/Doc/Release/Zsh-Line-Editor.html#Standard-Widgets)
