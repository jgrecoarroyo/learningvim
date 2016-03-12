# <img src="https://raw.githubusercontent.com/jgrecoarroyo/learningvim/master/img/vim_badge.png" data-canonical-src="https://raw.githubusercontent.com/jgrecoarroyo/learningvim/master/img/vim_badge.png" width="50" height="60" /> VIM

### vi improved

Note: this notes follow mainly the tutorial found in the CLI `vimtutor`

## Lesson 1 - The very basics


  1. To **start** Vim from the shell prompt type:  vim FILENAME `<ENTER>`
  2. To **exit** Vim type:     `<ESC>`   :q!   `<ENTER>`  to trash all changes.

         OR type:  <ESC>  :wq   <ENTER>  to save the changes.

  3. To **move the cursor** use either the arrow keys or the hjkl keys.

     ```
     h (left)       j (down)       k (up)       l (right)
     ```

  4. To **delete** the character at the cursor type:  x

  5. To **insert** or append text type:
         i   type inserted text   <ESC>         insert before the cursor
         A   type appended text   <ESC>         append after the line

NOTE: Pressing <ESC> will place you in Normal mode or will cancel an unwanted and partially completed command.



## Lesson 2 - Moving around

1. To **move page** forward / backward:

   ```
   page forward (Ctrl + f)                page backward (Ctrl + b)
   ```

2. To **move a block** up / down:

   ```
   block up (Ctrl + u)                block down (Ctrl + d)
   ```

3. To move to the beggining of the **next word** press `w`

4. To move to the **end** of the next word press `e`

5. To move to the **start of the line** use a zero:  `0`

## Lesson 3 - Deleting 

1. To **detele a character** press: `x`
2. To **delete a whole line** press: `dd`

## Lesson 4 - Repeating a motion

1. The format for a change command is:

              operator   [number]   motion
        where:
          operator - is what to do, such as  d  for delete
          [number] - is an optional count to repeat the motion
          motion   - moves over the text to operate on, such as  w (word),
                     $ (to the end of line), etc.

   ##### Examples

   1. To **move X number** of words press: `3w` (moves 3 words), `5e`, etc.
   2. To **delete X number** of times press: `2dd` (deltes 2 whole lines)

## Lesson 5  - Undo

1. To **undo** previous actions, type:                 `u  (lowercase u)`
2. To **undo all** the changes **on a line**, type:   `U  (capital U)`
3. To **undo the undo's**, type:  `<CTRL-R>`

## Lesson 6  - Put, Replace and Change 

1. **PUT** operator: press `p` (inserts line deleted with `dd`)
2. **REPLACE** operator: press `r`  and then the character you want to have there.
3. **CHANGE** operator: 
   1. type `ce`  to change from the cursor to the end of the word
   2. type `c$`  to change to the end of a line

   The format for change is: ```c   [number]   motion```

## Lesson 7 - Search command

1. ***Type  `/`  followed by a phrase to search for the phrase.*** 
   1. In Normal mode type the  /  character.  Notice that it and the cursor appear at the bottom of the screen as with the  :  command.
   2. To search for the same phrase again, simply type  n. To search for the same phrase in the opposite direction, type  N.
2. **Type `%` to find a matching ),], or }**
   1. Place the cursor on any (, [, or { 

   2. Now type the  %  character. The cursor will move to the matching parenthesis or bracket.

## Lesson 8 - Replace command

  1. To substitute new for the first old in a line type        ` :s/old/new`
  2. **To ask for confirmation each time add 'c'**             `:%s/old/new/gc`

## Lesson 9 - Run external command

1. **Type  `:!`  followed by an external command to execute that command.**
   1. Type the familiar command  :  to set the cursor at the bottom of the screen.  This allows you to enter a command-line command.
   2. Now type the  !  (exclamation point) character.  This allows you to execute any external shell command.
   3. As an example type   ls   following the ! and then hit `<ENTER>`.

## Lesson 10 - Visual selection `v`

To save part of the file, type  v  motion  :w FILENAME

  1. Move the cursor to this line.

  2. Press  v  and move the cursor to the fifth item below.  Notice that the
     text is highlighted.

  3. Press the  :  character.  At the bottom of the screen  :'<,'> will appear.

  4. Type  w TEST  , where TEST is a filename that does not exist yet.  Verify
     that you see  :'<,'>w TEST  before you press <ENTER>.

## Lesson 11 - Inserting text

1. **From an extrenal file**: type`:r FILENAME`  retrieves disk file FILENAME and puts it below the cursor position.
2. **Append** data: type `a`
3. **Insert** data: type `i`
4. **Open a new line** of data **BELOW** the cursor line: type `o`
5. **Open a new line** of data **ABOVE** the cursor line: type `<SHIFT> + o`
6. **Replace** more than one character: type `<SHIFT> + r`


## Lesson 12 - Copy & Paste

1. To **copy** use the operator `y`

2. To **paste** use the operator `p`

   *Note: to copy more than a line use the visual block operator `v`*


## Lesson 13 - Split screen

1. To **split the window** in two, type the command `:split`
   1. To split the window with another file type `:split file2.txt`
   2. To open a **new window** type `:new`
   3. To perform **vertical split** type `:vsplit`
2. To **switch** between windows type `<CTRL> + w`
3. To **close all** windows type the command `:close`
4. To **close all other** window type the command `:only`

Note: further reading type `:help usr_08.txt`

## Lesson 14 - Open file explorer

1. To open the file explorer type `:e`

   `

## Extra

### Highlight syntax

How to add syntax highlighting? use the command `:syntax on`

To add this change permanentely, you can edit ~/.vimrc file and append vim command syntax on to it. This ensures that vim will start with color syntax highlighting option on.





### Help

Just type `:help` inside vim, enjoy!

### Cheatsheet

<img src="http://zzyxx.wdfiles.com/local--files/tui-text-editors/vi-vim-cheat-sheet-belgian-azerty.svg">