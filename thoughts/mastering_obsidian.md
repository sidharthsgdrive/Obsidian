`24/06/25` This note is meant to facilitate my ongoing understanding of Obsidian. I'll note any ideas, videos, articles, or links that could be relevant to improving my usage of the tool here. 
* [Mastering Obsidian by FromSergio](https://www.youtube.com/playlist?list=PL7oLu8NfQd84_gsyqBVSVgUmCCgcvSZMx)
* It might be helpful to prefix file names with two- or three-letter keywords to make it easier to search for them.
* Coloring graph view:
	* - If you want to set a color for all the files with the tag cool, type `tag:#cool`
	- If you want to color all the files whose name begins with "journal", type `file:journal`
	*  If you want to color all the files in the "private" folder, type `path:private`
***
`28/06/25` I've been thinking about ways to mark files that I haven't written, for 
completion. What if I implement a solution in code somehow, to scan if files are empty and add it to a list of files in [[homepage]] or [[todolist]]? 
***
`01/07/25` I figured out how to resize images in Obsidian. Inside the brackets of the pasted image URL, add `|n` where n is an integer, to set image width. 
`08/07/25` I found out you can put images side by side by removing the \n after the image link.
***
`09/07/25` In the process of taking lecture notes for IIT Python, I figured out how to make proper code blocks (not just monospace).
```Python
n = int(input("Enter your number: "))
digits = [int(i) for i in str(i).split()]
```
`15/07/25` It seems for some languages like autohotkey, reading mode needs to be active for syntax highlighting to take effect.
***
`14/07/25` I accidentally discovered a feature of Obsidian that lets you pop out windows like you would on a browser. The windows persists after relaunch, but due to the setting causing the app to launch on the Daily Note, it defaults to that. to remedy this, I'll just disable that setting.
***
`15/07/25` After putting it off for a while, I got it in my head to finally investigate the Callouts feature. I installed the [Callout Manager](obsidian://show-plugin?id=callout-manager) plugin to help get familiarized with callouts, and to change the colours if needed. (btw, I linked this using the "copy share link" option on the plugin page -- this seems to be the only use for it)
I assigned the hotkey `Ctrl + Alt + Shift + C` to insert a callout, and also, rather adhoc, `Ctrl + F1` to clear formatting.
***
`16/07/25` Keeping up the theme of visual improvements for Obsidian, I found an Obsidian [forum post](https://forum.obsidian.md/t/caret-cursor-thickness/48969/9?u=zlzbub) on cursor customization, in which this guy posted some helpful CSS to alter the [Ninja Cursor](obsidian://show-plugin?id=ninja-cursor) plugin, removing the flashy animations and using it to make a smooth caret. I further modified it slightly to make the animation more obviously smooth, and changed the colour to an off-lilac to match my theme. The CSS snippet is noted in [ninjacursor].
`17/07/25` I messed around with the CSS a little more, to make it a block. Now Obsidian looks just like monkeytype lmao.
***
`19/07/25` I just realized there's a built-in button to reveal the current file in explorer navigation.
![[Pasted image 20250719104648.png#center|120]]
 
 I added a [CSS snippet](alignimages.md) to align images, sourced from [this video](https://www.youtube.com/watch?v=pDl418_Yj4w). I have used it in the above image -- it can be aligned `#left`, `#right`, and `#center.`
***
 `20/07/25` I installed the [Outliner](obsidian://show-plugin?id=obsidian-outliner) plugin that allows for reordering of items in a list via drag-and-drop. There is more functionality for this plugin though, so I have to follow up with a closer inspection, and find alternatives for drag-and-drop if the other features are not to my taste.
***
 `28/07/25` I created the #unique tag to catalogue interesting moments.
***
`30/07/25` Installed the [Extended Markdown Syntax](obsidian://show-plugin?id=extended-markdown-syntax) plugin, which allows for much more formatting flexibility, with options such as ++underline++, ^superscript^ and ~subscript~, ||spoilers||, and =={cyan}highlighting==.
***
`10/08/25` Installed the [Text Snippets](obsidian://show-plugin?id=text-snippets-obsidian) plugin. I had been looking for this feature for a while, and this will render the `symbols` and `malayalam` files obsolete. I've set the trigger key to `Shift + Space` and `Ctrl + Space`. The plugin space says you can set the space key on its own to fill in the text, but it doesnt' seem to be working. I should look into that in the future. Meanwhile, I should look into taking full advantage of this powerful new plugin. 
p.s. It seems the `Shift + Space` keybind causes conflicts with pressing the spacebar while holding shift, even if the previous word isn't a snippet. I'll disable that hotkey for now. 
***
`10/08/25` I reorganized [todolist] to include tasks from all fields. At some point, I should incorporate dataview to make it more intelligent and pull tasks from daily notes.
***
`04/09/25` installed the [relative line numbers](obsidian://show-plugin?id=obsidian-relative-line-numbers) plugin, in hopes of bettering my [[vim_motions]]. 
***
`16/09/25` Altered the Metrics template by replacing leading spaces with the Braille blank character, to enable easier navigation with Vim `f `.
***
`20/09/25` I renamed the timetable folder to [planning]
***
`11/11/25` It's been a long time I bothered to change the way I do things in Obsidian, and I propose linking to new notes I create, to the daily note of that day. Maybe I should do the same with this note.
`14/12/25` Crazy that it's taken me a month to implement this change, but I've renamed the "Thoughts" section to "Notes". Also, I'll be including modifications in the links, not just created dates.
[[260303-Tue]] It's crazy how It's taken me this long to think of it, but instead of linking to created notes from each daily note, why don't I just replace this clunky date-stamp system with directly linking to the day's daily note? That makes much more intuitive sense, and the files created or modified each day can be viewed through backlinks (`Ctrl+X` -> Outgoing Links)
