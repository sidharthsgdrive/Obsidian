qq++Modes++
`I` insert mode
`A` append mode, `Shift+A` append to current line
`V` visual mode, `Shift+V` select current line in visual mode
`Esc` normal mode

++Navigation++
`Shift+G` go to last line
`GG` go to first line
`+` go to beginning of next line
`^` go to beginning of line
`xj` / `xk` relative line navigation

++Focus++
`ZZ` focus current line to middle
`Shift+M` go to middle line on screen

++Deletion++
`0D` or `Shift+S` delete current line without linebreak
`dd` delete current line, including line break
`dtx` delete till and not including x
`diw` delete inside word

++Search++
`?x` search for x

++Replace++
`nrx` replaces next `n` characters with the character `x`

++Commenting++
`gc` comment selected in Visual mode
`gcc` comment current line in Normal mode
`gc{motion}` comment motion in Normal mode

++Indentation++
`>`

++Numbering++
`:set relativenumber!` toggle relative numbering