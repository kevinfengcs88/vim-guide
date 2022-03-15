# VIM Guide

Welcome to my guide to [VIM](https://www.vim.org/)! All of the code in this repository, including these Markdown files, will be written with
the [Vim extension for VSCode](https://marketplace.visualstudio.com/items?itemName=vscodevim.vim). To get started, install the extension. And...
you're pretty much done! From here, you can figure out your own preferences, if you need to enable macros, etc. One modification that I strongly recommend
is to enable "tab" functionality while in VIM's readonly mode. To do this, simply go to your `keybindings.json` file in VSCode. An easy way to get
to this file is to **ONLY USE YOUR KEYBOARD**. This is a VIM guide after all, so you may as well get used to abandoning that mouse of yours, until it's
time to play Valorant, of course. To open `keybindings.json`, I recommend doing the following:

- `CTRL + SHIFT + P`: this opens up the VSCode command palette
- Type in "open key": at this point, the `keybindings.json` file should pop up as one of the options
- Hit `ENTER` if the option to open `keybindings.json` is already selected
- Otherwise, use the down arrow key as many times as necessary to select it

Congratulations! You're on your way to becoming a true keyboard warrior. But not *that* type of keyboard warrior. I'd strongly advise against having virtual
arguments with strangers on the internet over social media platforms. Trust me. Now that we've gotten to the `keybindings.json` file, let's enable
"tab" functionality for readonly mode while in VIM. You've probably already noticed how your normal cursor in VSCode has disappared, only to be
transformed into a blinking highlight, like those found in terminals. Since this is a guide to VIM, I'll be writing up documentation on what I belive to
be the most important commands, but for now, here are a few basic ones to get you started (and actually be able to make some changes to `keybindings.json`).

- `i` : Enter insert mode on the left side of the readonly highlight
- `a` : Enter insert mode on the right side of the readonly highlight
- `CTRL + C` : Exit insert mode (the main command is `ESC`, but as programmers, hitting the "copy" macro is already hard-wired into our brains, so why not stick with that one?)
- `j` : Go down one line
- `k` : Go up one line
- `l` : Go right one character
- `h` : Go left one character

There are quite a few more basic commands, but this is a good starting point. Getting used to the directions associated with your home row keys and quickly
toggling between readonly and insert mode should be your initial goal. Now let's insert some JSON data:

```
[
   {
       "key": "tab",
       "command": "tab",
       "when": "editorTextFocus && !editorTabMovesFocus"
   },
   {
        "key": "shift+tab",
        "command": "outdent",
        "when": "editorTextFocus && !editorTabMovesFocus"
   }
]
```

The brackets may already be in the file.