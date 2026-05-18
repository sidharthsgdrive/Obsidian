`22/08/25` A few months ago, I had disabled tab groups using a method provided by a reddit user on [this thread](https://www.reddit.com/r/firefox/comments/1jvln5l/how_to_disable_tab_grouping/). The comment advised creating a `policies.json` file in the following path:
`C:\Program Files\Mozilla Firefox\distribution`

```json
{
    "policies": {
      "Preferences": {
        "browser.tabs.groups.enabled": {
          "Value": false,
          "Status": "locked"
        }
      }
    }
  }
```

However, Firefox has recently added a feature that uses a local AI model to autogroup tabs. I think I'll try this feature out, so I'm temporarily deleting the contents of the policies file.
***
`22/08/25` Over the past few days, I've been experimenting with the search engines feature of Firefox. I got keyword-based search engines working for both Perplexity `perp` and PStream `pstream`.
***
`25/08/25` Added the [Mouse Pinch-To-Zoom](https://addons.mozilla.org/en-US/firefox/addon/mouse-pinch-to-zoom/) extension which allows touchpad-style zooming with the scrollwheel while holding `LAlt`.
***
`12/11/25` Installed the  [GX Theme Styles](https://addons.mozilla.org/en-US/firefox/addon/gx-theme-styles/) extension, which allows for custom theming.