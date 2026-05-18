`15/07/25` I used an AHK script provided in [this](https://www.autohotkey.com/boards/viewtopic.php?t=83471) forum post to rebind RAlt + IJKL to the arrow keys. (switch to reading mode to enable syntax highlighting)

```autohotkey
global LevelFive
LevelFive = false

EnableLevelFive()
{
    LevelFive = true
}

DisableLevelFive()
{
    LevelFive = false
}

IsLevelFive()
{
    return %LevelFive% = true
}

*RAlt::
    EnableLevelFive()
return

*RAlt up::
    DisableLevelFive()
return

#If IsLevelFive()
    ; arrow keys
    i::up
    j::left
    k::down
    l::right

    ; home & end
    ; u::home
    ; o::end

    ; page up & page down
    ; [::PgUp
    ; '::PgDn
    
    ; quotation marks
    ; [::send, “
    ; ]::send, ”
#If
```

`04/08/25` I extended the functionality to home, end, pgup, and pgdown. Note that the backtick is used as the escape character in AHK.

```
global LevelFive
LevelFive = false

EnableLevelFive()
{
    LevelFive = true
}

DisableLevelFive()
{
    LevelFive = false
}

IsLevelFive()
{
    return %LevelFive% = true
}

*RAlt::
    EnableLevelFive()
return

*RAlt up::
    DisableLevelFive()
return

#If IsLevelFive()
    ; arrow keys
    i::up
    j::left
    k::down
    l::right

    ; home & end
    p::home
    `;::end

    ; page up & page down
    [::PgUp
    '::PgDn
    
    ; quotation marks
    ; [::send, “
    ; ]::send, ”
#If
```

`06/08/25` I further extended the functionality to include the right and left clicks via `RAlt+O` and `RAlt+U` respectively.

```autohotkey
global LevelFive
LevelFive = false

EnableLevelFive()
{
    LevelFive = true
}

DisableLevelFive()
{
    LevelFive = false
}

IsLevelFive()
{
    return %LevelFive% = true
}

*RAlt::
    EnableLevelFive()
return

*RAlt up::
    DisableLevelFive()
return

#If IsLevelFive()
    ; arrow keys
    i::up
    j::left
    k::down
    l::right

    ; left & right click
    u::LButton
    o::RButton

    ; home & end
    p::home
    `;::end

    ; page up & page down
    [::PgUp
    '::PgDn
    
    ; quotation marks
    ; [::send, “
    ; ]::send, ”
#If
```

`11/08/25` I further changed the arrow keys rebind to use hjkl instead of ijkl, in accordance with the Vim keybinds, since I plan to learn Vim at some point.

```autohotkey
global LevelFive
LevelFive = false

EnableLevelFive()
{
    LevelFive = true
}

DisableLevelFive()
{
    LevelFive = false
}

IsLevelFive()
{
    return %LevelFive% = true
}

*RAlt::
    EnableLevelFive()
return

*RAlt up::
    DisableLevelFive()
return

#If IsLevelFive()
    ; arrow keys
    j::up
    h::left
    k::down
    l::right

    ; left & right click
    u::LButton
    o::RButton

    ; home & end
    p::home
    `;::end

    ; page up & page down
    [::PgUp
    '::PgDn
    
    ; quotation marks
    ; [::send, “
    ; ]::send, ”
#If
```