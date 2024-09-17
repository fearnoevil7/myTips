# Tmux default key mappings.

- Create and attach to a new session.
    - $ `tmux`
    - $ `tmux new`

<br>

- Create and attach to a new session named NAME_HERE.
    - $ `tmux new -s NAME_HERE`

<br>

- How to reattach to the previous session.
    - $ `tmux attach`
    - $ `tmux a`

<br>

- Attach to tmux session named NAME_HERE.
    - $ `tmux a -t NAME_HERE`

<br>

- View all active tmux sessions.
    - $ `tmux ls`

<br>

- Leader
    - `Ctrl + b`

<br>

- Create a new window.
    - `<Leader> -> c`

<br>

- Switch to next window.
    - `<Leader> -> n`

<br>

- Switch to a specific window.
    - `<Leader> -> <Window #>`

<br>

- Split window vertically.
    - `<Leader> -> %`

<br>

-  Split window horizontally.
    - `<Leader> -> "`

<br>

- Enter command mode.
    - `<Leader> -> :`

<br>

- Enter the following command into the tmux command prompt to rename a window.
    - :`rename-window`

<br>

- How to detach from a tmux-session.
    - `<Leader> -> d`

<br>

- How to start a tmux session.
    - $ `tmux`

<br>

- How to list all current tmux sessions.
    - `<Leader>` -> s

<br>

- Enter ***copy mode***, and enable scrolling in currently-opened tmux session. Press `q` to exit.
    - `<Leader>` -> s

<br>

- Enter the following command into the tmux command prompt to rename a sessions.
    - :`rename-session`

<br>

- Enter the following command into the tmux command prompt to kill current sessioni.
    - :`kill-session`

<br>

- Kill current pane.
    - `<leader>` -> x

<br>

- Toggle maximization of current pane.
    - `<leader>` -> z

<br>

- Show pane numbers.
    - `<leader>` -> q

<br>

- Resize all panes to equal size.
    - `<leader>`, ESC, 2

<br>

- List all tmux keybindings.
    - $ `tmux list-keys`
