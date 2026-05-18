`25/08/25`  It seems I had made a mistake when remapping `HJKL` using AHK -- in Vim, `j` is `down` and `k` is `up`. This means I'll have to relearn the muscle memory for that. Anyway, here's the `default.conf` contents in `/etc/keyd`.

The manual can be accessed using `man keyd`. 

```keyd
[ids]

*

[main]

rightalt = layer(nav)

[nav]

h = left
j = down
k = up
l = right
```

***

`28/08/25` reintroduced the default keyd mapping of `CapsLock` to `Esc` when pressed and `Ctrl` when held, to facilitate Vim motions.
Edit: Removed the Ctrl binding, because 
1. I don't have a need for it
2. It interferes with some Vim motions on accident
***
`24/12/25` Added LMB and RMB support
```keyd
[ids]

*

[main]

rightalt = layer(nav)

# Maps capslock to escape when pressed and control when held.
capslock = esc

# Remaps the escape key to capslock
esc = capslock

[nav]

h = left
j = down
k = up
l = right
u = leftmouse
i = middlemouse
o = rightmouse

```