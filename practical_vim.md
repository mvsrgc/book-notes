## Practical Vim, Second Edition

### Make corrections instantly from insert mode

  * <C-h\> : Delete back one character
  * <C-w\> : Delete back one word
  * <C-u\> : Delete back to start of line

### Compose repeatable changes

  * daw and dap are more repeatable than dbx and bdw

### Favor repeatability over counting

  * To delete 7 words, favor dw...... over d7w

### Incrementing numbers

  * <C-a\> adds a count to the number at or after the cursor, which means it can look ahead for a digit on the current line
  
### Paste from a register without leaving insert mode

  * <C-r\>0 pastes the last yanked text
  
### Expression register for back-of-the-envelope math

  * <C-r\>=
  
### Line-wise vs. character-wise visual mode

  * V is line-wise and v is character-wise

### Visual selection

  * o goes to the other end of the highlighted text (really handy if you realize during a selection that you started in the wrong place)
  * Prefer gUit to vitU (the former is more repeatable because it is considered 1 command [gUit], whereas the latter is 2 commands [vit, U])

### Netrw

  * [:help netrw-quickmap](https://vimhelp.org/pi_netrw.txt.html#netrw-quickmaps)

### Windows

  * <C-w\><C-w\> does the same thing as <C-w>w. That means you can hold the ctrl key and press ww to change window.
  * <C-w\>c closes the active window (alternative to :q)
  * <C-w\>o closes all other windows

### Save file to nonexistent directory

  * :e madeup/dir/doesnotexist.txt
  * :write `Error can't open file for writing`

  * :e madeup/dir/doesnotexist.txt
  * :! mkdir -p %:h
  * :write

### Real line vs display line

  * {j,k,h,l} navigate real lines
  * g{j,k,h,l} navigate display lines

### Combining d operator with the search motion is a power move

### Hack to jump back to most recent change

  * u<C-r> does and undo and then a redo, which cancel each other out but place our cursor
    on the last change

### Global mark

  * mM sets a global mark that allows to jump between files
