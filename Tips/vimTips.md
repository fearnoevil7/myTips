# Vim Tips & CheatSheet

# Working with code folds.
- `zR` ***open all folds***
- `zM` ***close all folds***
- `zA` ***toggles the fold at the cursor***
- `zk` ***move up/down to the next fold***
- `zj` ***move up/down to the next fold***


<br>

# Working with multiple files (buffer commands)
 - `:e[dit]` file - edit a file in a new buffer.
 - `:bn[ext]` - go to the next buffer.
 - `:bp[revious]` - go to the previous buffer.
 - `:bd[elete]` - delete a buffer (close a file)
 - `:b[uffer]#` - go to a buffer by index #
 - `:ls` or :buffers - list all open buffers.

<br>

# Ranges
- Here are the most interesting ranges you can use:
    - `.` - Represent the current line (often the default range).
    - `$` - Represent the last line of the current buffer.
    - `%` - Represent the entire file (same as 1,$).
    - `*` - Use the last selection you’ve made during the last VISUAL mode.
- For example, using the command :d:
    - `:1,40d` - Delete line 1 to 40 included.
    - `:2,$d` - Delete every line from the second one till the end of the file.
    - `:.,$d` - Delete every line from the current one till the end of the file.
    - `:%d` - Delete every line.

<br>

# Jumplist
- Each time we use a jump motion, ***the position of the cursor before the jump is saved in the jump list.*** You can move through this jump list with the following keystrokes:
    - `CTRL-o` - Go to the previous (older) cursor position.
    - `CTRL-i` - Go to the next cursor position (i is near o).
    - `:help jumplist`, `:help jump-notations` - help

<br>

-  ***You can move from line to line and even from buffer to buffer with these holy commands.*** I use them all the time, and you will, too.
-  To display your jump list, use the command `:jumps`.

<br>

# Changelist
- Another useful list is the change list. Each time you insert something (using `INSERT` mode), ***the position of your cursor is saved in the change list***.
    - `:help changelist` - help
        - You can navigate through the change list using these keystrokes.
        - `g;` - Jump to the next change.
        - `g,` - Jump to the previous change

- Discovering them was like seeing the light for the first time.

<br>

- Since we’re developers, it’s nice to be able to jump from method to method. You can do that with the following keystrokes:
    - `[m` - move to the start of a method.
    - `]m` - move to the end of a method.

<br>

# You can access the history of your Ex commands directly in Vim
- `q:` - Open command line history.
- `q/` - Open search history.
- `CTRL + f`
    - `:help cmdline-window`, `:help 'history` - help

<br>

- Open Command line history while in COMMAND LINE mode.
    - If you don't like the keystroke `CTRL + f` open to open the command line history, ***you can change it by changing the value of the option*** `cedit`. The value by default is `^f` `CTRL + F`.

<br>

# Advanced
# Vim's Quickfix And Location List
- Don’t ***confuse the quickfix list and the quickfix window:*** these are two different entities. The first is a data structure, the second can display this data structure.

<br>

# Quickfix list
- You can think of a quickfix list as a set of positions in one or multiple files.

<br>

- Let’s take an example: what happens if you run the command `:vimgrep hello *?`
    1. It will search the pattern ***“hello”*** in every file of your working directory.
    2. It will populate a quickfix list with every position matching your pattern ***“hello”***.
    3. It will move your cursor to the ***first position*** of the quickfix list.

- If you want to know more about vimgrep and other tools you can search with, [I wrote an article about that.](https://thevaluable.dev/vim-search-find-replace/) Other commands (like `:make` or `:grep`) also populate automatically a quickfix list.

<br>

- The quickfix list is often used to display specific errors in a codebase, often spit out from a compiler or a linter (via the command `:make` for example), but not only, as we just saw. I call the entries of a quickfix list ***“positions”*** to be more general, but sometimes Vim’s help will refer to them as ***“errors”***. Don’t be confused: it’s the same idea. 
    - Among other conditions, a quickfix list entry needs to have a filename for you to be able to jump to its position. Otherwise, the entry doesn’t point to anything.

<br>

- Here are the commands you can use to navigate through the current quickfix list:
    - `:cl or :clist` - Display all valid entries of the current quickfix list. You can add a range as argument (only numbers).
    - `:cc <number>` - Move to the ***<number>th*** entry of the current quickfix list.
    - `:cnext or :cn` - Move to the next entry of the current quickfix list.
    - `:cprevious or :cp` - Move to the previous entry of the current quickfix list.
    - `:cfirst or :cfir` - Move to the first entry of the current quickfix list.
    - `:clast or :clas` - Move to the last entry of the current quickfix list.

<br>

Here are additional commands which make quickfix lists really powerful:
    - `:cdo <cmd>` - Execute a command <cmd> on each valid entry of the current quickfix list.
    - `:cexpr <expr> or :cex <expr>` - Create a quickfix list using the result of evaluating the Vimscript expression <expr>.
    - `:caddexpr <expr> or :cadde <expr>` - Appends the result of evaluating the Vimscript expression <expr> to the current quickfix list.

<br>

If you have no clue how to use the last two commands, you can do for example:
    - `:cex []` - Empty the current quickfix list.
    - `:cex system("<cmd>")` - Populate your quickfix list with any ***shell command*** `<cmd>`. You can try it with `ls` for example.

# Quickfix Window
- What about displaying the current quickfix list in a new buffer? You can do that with the following command:
    - `:copen or :cope` - Open a window (with a special buffer) to show the current quickfix list.
- ***You can only have one quickfix window open.*** To move to the position of the selected entry of the quickfix list in the quickfix window, hit `ENTER` or `.cc`.

<br>

# Location Lists
- A location list is similar to a quickfix list, except that the first is local to a window and the second is global to your Vim instance. In other words, you can have multiple location lists available at the same time (one per window open), but you can only have access to one quickfix list.    

<br>

- The commands for location lists are similar to the ones for the quickfix lists; often, you’ll only have to replace the first ***c (quicfix)*** of the command with ***l (location)***.
    - For example:
        - `:lli or :llist` - Display all valid entries of the current location list. You can add a range as argument (only numbers).
        - `:ll <number>` - Move to the entry <number> of the current location list.
        - `:lnext or :lne` - Move to the next entry of the current quickfix list.
- ***To populate your location list you can also use the commands*** `:lvimgrep` or `:lmake` for example.

<br>

- Often, Vim users will use the quickfix list for anything related to errors in their codebase, and the location list for search results. But it’s up to you at the end of the day. With Vim, you’re the master of your destiny.
    - `:help quickfix`, `:help quickfix-window`, `:help location-list`, `:help quickfix-window`, `:help quickfix-window`, `:help quickfix-window` - help

<br>

# Appending a Recording
- If you ***made a mistake during the recording of a macro***, you can spit the whole register, modify it, and save it back.

<br>

- You can ***append to your recording by using the uppercase variant of your register***. For example:
    1. Hit `qa` and record whatever keystrokes you want. Stop the recording by hitting `q` again.
    2. You realize that you forgot a couple of keystrokes.
    3. Execute your keystrokes to be sure you’re at the last position of your recording.
    4. Hit `qA` to append to your register `a`. When you’re done, hit `q` again.
<br>

# The Substitute Commands

- [Go here.](https://thevaluable.dev/vim-advanced/)

<br>

# Helpful Links
- [Vim Cheatsheet](https://www.barbarianmeetscoding.com/boost-your-coding-fu-with-vscode-and-vim/cheatsheet/)
- [The Valuable Dev: A Guide For Intermediate Users](https://thevaluable.dev/vim-intermediate/)
- [The Valuable Dev: A Guide For Advanced Users](https://thevaluable.dev/vim-advanced/)
- [Neovim: Lua-guide](https://neovim.io/doc/user/lua-guide.html#lua-guide-modules)
