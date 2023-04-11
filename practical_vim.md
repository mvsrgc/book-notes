## Practical Vim, Second Edition


### Make corrections instantly from insert mode

#### Keystrokes:
  * \<C-h\> : Delete back one character
  * \<C-w\> : Delete back one word
  * \<C-u\> : Delete back to start of line

### Compose repeatable changes

#### Keystrokes:
  * daw and dap are more repeatable than dbx and bdw

### Favor repeatability over counting

  * To delete 7 words, favor dw...... over d7w

### Incrementing numbers

  * \<C-a\> adds a count to the number at or after the cursor, which means it can look ahead for a digit on the current line
