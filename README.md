# VIM

### vi improved

Note: this notes follow mainly the tutorial found in the CLI `vimtutor`



## Lesson 1 SUMMARY


  1. To **start** Vim from the shell prompt type:  vim FILENAME <ENTER>
  2. To **exit** Vim type:     <ESC>   :q!   <ENTER>  to trash all changes.

         OR type:  <ESC>  :wq   <ENTER>  to save the changes.

  3. To **move the cursor** use either the arrow keys or the hjkl keys.

     ```
     h (left)       j (down)       k (up)       l (right)
     ```

  4. To **move page** forward / backward:

     ```
     page forward (Ctrl + f)                page backward (Ctrl + b)
     ```

  5. To **delete** the character at the cursor type:  x

  6. To **insert** or append text type:
         i   type inserted text   <ESC>         insert before the cursor
         A   type appended text   <ESC>         append after the line

NOTE: Pressing <ESC> will place you in Normal mode or will cancel an unwanted and partially completed command.



## Extra

### Highlight syntaxt

How to add syntax highlighting? use the command `:syntaxt on`

To add this change permanentely, you can edit ~/.vimrc file and append vim command syntax on to it. This ensures that vim will start with color syntax highlighting option on.



### Cheatsheet

<img src="https://raw.githubusercontent.com/jgrecoarroyo/learningvim/master/img/vimCheatsheet1.svg">



