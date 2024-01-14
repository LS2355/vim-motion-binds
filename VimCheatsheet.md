//this is the cheat sheat for all of the vim commands 
✨ - featured / important



//movement
✨move cursor left  - h
✨move cursor right - l 
✨move cursor down  - j
✨move cursor up    - k

✨move to top of screen    - H
✨move to middle of screen - M
✨move to bottom of screen - L

✨jump fowards to start of word                          - w
✨jump fowards to start of word  (including punctuation) - w

✨jump fowards to End of word                         - e 
✨jump fowards to End of word (including punctuation) - E 

✨jump backwards to start of word                         - b
✨jump backwards to start of word (including punctuation) - B

✨jump to the start of the line                           - 0
jump to the first non-blank character of the line          - ^
✨jump to the end of the line                             - $
jump to the last non-blank character of the line           - g_

✨go to first line in document                            - gg
✨go to last line in document                             - G 
✨go to line 5                                            - 5G (works with any line) 
✨jump to next occurrence of character x                  - fx (works with any char)
✨jump to before next occurrence of character x           - tx (work with any char)
✨jump to next paragraph,function, or block               - <!--}-->
✨jump to previous paragraph, function, or block          - <!--{--> 
✨center cursor on screen - zz



move back one full screen   - ctrl + b
move foward one full screen - ctrl + f
move foward 1/2 a screen    - ctrl + d
move back 1/2 a screen      - ctrl + u

//insert mode

✨stop inserting text           - esc
✨insert before the cursor      - i
✨insert at begining of line    - I
✨insert after the cursor       - a
✨insert at the end of the line - A 
✨insert at the end of the word - ea

✨append a new line below the current line - o
✨append a new line above the curretn line - O

✨delete the character before the cursor - ctrl + h
✨delete the word before the cursor      - ctrl + w

✨begin new line - ctrl + j

✨indent line one shiftwidth   - ctrl + t
✨de-indent line one shifwidth - ctrl + d

✨insert (auto complete) next match before the cursor    - ctrl + n
✨insert (auto complete) previous math before the cursor - ctrl + p
insert contents of register x                            - ctrl + rx

✨temporarily enter normal mode to issue one normal mode command x - ctrl + ox

//editing
✨replace a single character                             - r 
✨replace more than one character (until esc is pressed) - R

✨join line below to the current one with one space in between - J
✨join line below to the current one without space in between  - gJ
reflow paragraph                                               - gwip

✨switch case up to motion          - g~
✨change to lowercase up to motion  - gu
✨ change to uppercase up to motion - gU

change (replace entire line)              - c$ or c
change (replace) entire word              - ciw
✨change (replace) to the end of the word - cw or ce
✨delete character and substitute text    - s 
✨delete line and sustitute text          - S
✨delete and paste                        - xp

✨undo                            - u
✨restore (undo) last change line - U
✨redo                            - ctrl + r
repeat last command               - .



//marking text

exit visual mode                                               - esc
✨start visual mode, mark lines, then do a command (like y-yank) - v
✨start linewise visual mode                                     - V
✨move to other end of marked area                               - o 
✨start visual block mode                                        - ctrl + v
move to other corner of block                                    - O
✨mark a word                                                    - aw
✨a block with ()                                                - ab
✨a block with {}                                                - aB
✨a block with <> tags                                           - it

//visual commands (in visual mode)

✨shift text right   - >
✨shift text left    - <
✨copy marked text   - y
✨delete marked text - d

✨switch case                     - ~
✨change marked text to lowercase - u
✨change marked text to uppercase - U

//registers 
show registers content                   - :ref[isters]
copy into register x                     - "xy
paste contents of register x             - "xp
copy into the system clipboard register  - "+y
paste from the system clipboard register - "+p

    //Tip 
      registers are being stored in ~/viminfo, and will be loaded again on next restart of vim 
    //Tip (special registers)
      0 - last yank
      " - unnamed register, last delete or yank
      % - current file name
      # - alternate file name
      * - clipboard contents (X11 primary)
      + - clipboard contents (X11 clipboard)
      / - last search pattern
      : - last command-line
      . - last inserted text
      - - last small (less than a line) delete
      = - expression register
      _ - black hole register
      
//mark and positions 

✨list of marks                 - :marks
set current position for mark A - ma
jump to position of mark A      - `a
yank text to position of mark A - u`a

go to the position where Vim was previously exited - `0
✨go to the position when last editing this file  - `"
go to the position of last editing this file       - `.
✨go to the position before the last last jump    - ``

list of jumps                       - :ju[mps]
go to newer position in jump list   - ctrl + i
go to olser position in jump list   - ctrl + o
list of changes                     - :changes
go to newer position in change list - g
go to older position in change list - G;
jump to tag under cursor            - ctrl + ]

// macros
record macro a       - qa
stop recording macro - q
run macro a          - @a
retun last run macro - @@



//cut and paste
✨copy a line                                                                            - yy
✨copy 2 lines                                                                           - 2y
✨copy the characters of the word from the cursor position to the start of the next word - yw
✨copy word under the cursor                                                             - yiw
✨copy word under the cursor and the space after or before it                            - yaw
✨copy to the end of the line                                                            - Y or Y$

✨paste before cursor                                                   - P (that capital P)
✨paste after cursor                                                    - p
✨paste the clipboard before cursor and leave cursor after the new text - gp
✨paste the clipboard after cursor and leave cursor after the new text  - gP

✨delete (cut) a line                                             - dd 
✨delete (cut) 2 lines                                            - 2dd
✨delete (cut) word under cursor                                  - diw
✨delete (cut) word under cursor and the space after or before it - daw
✨delete (cut) to the end of the line                             - D or $d
delete (cut) character                                             - x



//indent text 
✨indent (move right) line one shiftwidth                            - >>
✨de-indent (move right) line one shiftwidth                         - <<
✨index a block width () or {} (cursor on brace) line one shiftwidth - >%
indent inner block with ()                                            - >ib
indent a block with <> tags                                           - >at

re-indent 3 lines                                 - 3==
re-indent a block with () or {} (cursor on brace) - =%
re-indent inner block with {}                     - =iB
re-indent entire buffer                           - gg=G
✨paste and adjust indent to current line        - ]p



//exiting 
✨write (save) the file, but dont exit      - :w
write out the current file using sudo        - :w !sudo tee %
✨write (save and quit)                     - ZZ or :x or :wq or
✨quit (fails if there are unsaved changes) - :q
quit and throw away unsaved changes          - :q! or ZQ
write (save) and quit on all tab             - :wqa or ZQ

//search and replace
✨search for pattern                                     - /pattern 
✨search backward for pattern                            - ?pattern
repeat search in same direction                           - n
repeat search in opposite direction                       - N
replace all old with new throught file                    - :%s/old/new/g
replace all old with new throught file with confirmations - :%s/old/new/gs
remove highlighting of search matches                     - :noh[lsearch]



//diff

✨toggle folder under the cursor           - za
✨open fold under the cursor               - zo 
✨close fold under the cursor              - zc
✨reduce (open) all fold by one level      - zr
✨fold more (close) all folds by one level - zm
✨toggle folding functionality             - zi
jump to start of next change               - ]c
junp to start of previous change           - [c

    //tip 
    the commands for folding operate on one leveo. To operate on all levels, use uppercase letters



