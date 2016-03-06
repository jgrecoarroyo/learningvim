# VIM

### vi improved

Note: this notes follow mainly the tutorial found in the CLI `vimtutor`



## Lesson 1 - The very basics


  1. To **start** Vim from the shell prompt type:  vim FILENAME <ENTER>
  2. To **exit** Vim type:     <ESC>   :q!   <ENTER>  to trash all changes.

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
3. To **undo the undo's**, type:  <CTRL-R>







## Extra

### Highlight syntaxt

How to add syntax highlighting? use the command `:syntaxt on`

To add this change permanentely, you can edit ~/.vimrc file and append vim command syntax on to it. This ensures that vim will start with color syntax highlighting option on.



### Cheatsheet

<img
src="https://github.com/jgrecoarroyo/learningvim/img/vimCheatsheet1.svg">



