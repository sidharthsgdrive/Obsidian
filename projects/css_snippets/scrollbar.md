`07/09/25` I was bothered by the huge scrollbars in the Iridium theme, so I looked online for solutions.
A comment on [this reddit post](https://www.reddit.com/r/ObsidianMD/comments/1k16mm6/css_snippet_to_change_scroll_bar/) suggested adding the following CSS snippet:

```CSS
body:not(.native-scrollbars) ::-webkit-scrollbar {
	width: 12px;
}
```

However, this seems to have removed the scrollbar altogether. 
Ah well, I'll keep it like that, since I don't have a use for the scrollbar anyway.
***
`12/09/25` For some reason, the changes I made the other day seem to have taken effect now, with extremely wide 30px scrollbars that I can't believe I didn't notice for days.
I edited the snippet again to remove it completely though, since like I stated before, I don't really use scrollbars all that much.