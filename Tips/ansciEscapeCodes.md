- ANSI escape codes offer a variety of formatting and color options for text in the terminal. Here's a rundown of some common ANSI escape codes and their uses:
Text Attributes:
    - Reset: `\033[0m` resets all attributes to their defaults.
    - Bold: `\033[1m` or \033[01;1m makes text bold.
    - Dim: `\033[2m` makes text dim (if supported).
    - Underline: `\033[4m` makes text underlined.
    - Blink: `\033[5m` makes text blink (if supported).
    - Inverse: `\033[7m` inverts the foreground and background colors.
    - Hidden: `\033[8m` hides the text (often used for passwords).
    - Strikethrough: `\033[9m` strikes through the text (if supported).

<br>

# Text Colors:
- Foreground (text) color: `\033[38;5;<color_code>m` sets the text color to a 256-color mode color code.

<br>

- Background color: `\033[48;5;<color_code>m` sets the background color to a 256-color mode color code.
    - Standard colors:
    - Black: `\033[30m`
    - Red: `\033[31m`
    - Green: `\033[32m`
    - Yellow: `\033[33m`
    - Blue: `\033[34m`
    - Magenta: `\033[35m`
    - Cyan: `\033[36m`
    - White: `\033[37m`

<br>

# 256-Color Mode:
    - Color mode: `\033[38;5;<color_code>m` for foreground and `\033[48;5;<color_code>m` for background. `<color_code>` ranges from 0 to 255.

<br>

# True Color Mode:
    - True color (24-bit): `\033[38;2;<r>;<g>;<b>m` for foreground and `\033[48;2;<r>;<g>;<b>m` for background. `<r>`, `<g>`, `<b>` are red, green, and blue values ranging from 0 to 255.

<br>

# Cursor Positioning:

 - ***Move cursor***:
    - `\033[<line>;<column>H` moves the cursor to the specified line and column.1

<br>

 - ***Save cursor position***:
    - `\033[s` saves the current cursor position.
<br>

 - ***Restore cursor position***:
    - `\033[u` restores the saved cursor position.

<br>

# Erasing Text:
    - Clear screen:
        - `\033[2J` clears the entire screen.
<br>

    - Clear line:
        - `\033[K` clears the current line from the cursor position to the end.

<br>

- These are some of the most commonly used ANSI escape codes for text formatting and coloring in terminals. They allow for a wide range of customization when outputting text in the terminal.



- Sample Commmands:
    - `echo -e "[32mWHAM[0m"`
