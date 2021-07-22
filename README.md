# VS Code keymaps for Sublime Text 3
### or, "the ongoing struggle of making all text editors as comfortable as possible" 
---

I just started using [Sublime Text 3](https://www.sublimetext.com) for taking notes, and as a (great) replacement for `notepad.exe` in Windows.  

I use [VS Code](https://code.visualstudio.com/) for coding.  I'd used it for text editing a bit, but my installation has gotten too heavy with extensions to really be considered "light" enough for simple text editing duties.  

I like the keybindings and tab size control of Sublime Text 3,  the extensibility, the fact that you can change so much of it (with settings like these), and that it already feels so comfortable out of the box (VS Code *is* basically a highly successful rip-off of Sublime Text, after all).  So, this fork is an attempt to make it "feel" as much like VS Code as possible without becoming a cumbersome, slow-loading semi-IDE, as VS Code has become. 

There are a lot of [Sublime-to-VSCode keymap packages](https://marketplace.visualstudio.com/items?itemName=ms-vscode.sublime-keybindings) out there, but there didn't seem to be any going the other way, until I found this one from [jennynz](https://github.com/jennynz/vscode-keybindings-for-sublime), which had been updated by[yasapurnama](https://github.com/yasapurnama/vscode-keybindings-for-sublime).

 - [Compare]((https://github.com/jennynz/vscode-keybindings-for-sublime/compare/master...yasapurnama:master))

 So far, I have only added keybindings for duplicating lines in Windows and Linux, but I intend to add other keybindings as I discover they are not behaving in the same way I would expect after coming from VS Code:

 ```
// Default (Windows).sublime-keymap

        {"keys": ["alt+shift+down"], "command": "duplicate_line" },
        {"keys": [ "alt+shift+up"], "command": "duplicate_line" }


 ```

 ```
// Default (Linux).sublime-keymap

        {"keys": ["ctrl+alt+shift+down"], "command": "duplicate_line" },
        {"keys": [ "ctrl+alt+shift+up"], "command": "duplicate_line"}

 ```

Navigate to the file on this repo page that correponds to your OS platform, hit "raw", copy the page and paste it into the window on the right in `Preferences => Keybindings` menu in Sublime Text
(I recommend not editing the default settings on the left)

You can grab my preferences, too, if you like.  These are added in the same way as keybindings, but under `Preferences => Settings` 

 ```
//  Preferences.sublime-settings

{
        "color_scheme": "Monokai.sublime-color-scheme",
        "font_size": 11,
        "tab_size": 2,
        "ignored_packages":
        [
                "Vintage"
        ],
        "theme": "Adaptive.sublime-theme"
}

 ```



 Jennynz said she uses the [Zettelklasten method](https://zettelkasten.de/) for note-taking, which looks very interesting - I recommend checking it out (it's quite comprehensive). 

 The rest of this README was written by her:

 [this Sublime Text extension](https://github.com/renerocksai/sublime_zk) has been the best tool that I've found that it. I prefer VS Code as a text editor, so I want to stay familiar with their main key bindings while being able to use this Zettelklasten Sublime plugin.

I've picked and chosen the key bindings which I use the most, so if you have any other key bindings you'd like to recommend, please raise an issue.

## Installation

### Key bindings

1. Copy the key bindings from the `*.sublime-keymap` file that suits your operating system.
2. Open `Preferences` > `Key Bindings`.
3. Paste the key bindings into `Default (*).sublime-keymap - User`

### Settings

This is just to turn on the `shift_tab_unindent` setting, which is set to `false` by default on Sublime Text.

1. Copy the setting from [Preferences.sublime-settings](Preferences.sublime-settings).
2. Open `Preferences` > `Settings`.
3. Paste the setting into `Preferences.sublime-settings - User`

I would also recommend installing [MoveTab](https://github.com/SublimeText/MoveTab) and [GotoTab](https://github.com/SublimeText/GotoTab) packages for Chrome-like behaviour. You can do this via Package Control (`ctrl+shift+p` > `Package Control: Install Package` and search `MoveTab` and `GotoTab`).

## Usage

Only the key bindings for Windows have been tested. Please raise an issue or submit a pull request if any of these aren't working on Linux or OSX.

### Windows & Linux

- `ctrl+shift+l`: Select all instances of the current selection in file (`find_all_under`)
- `ctrl+f2`: Select all instances of the current selection in file (`find_all_under`)
	+ N.B. The default keymap for Sublime Text already allows `ctrl+d` to expand the selection to include the current selection's next occurrence.
- `alt+shift+i`: Split a multi-line selection into multiple lines (`split_selection_into_lines`)
- `ctrl+b`: Toggle the sidebar (`toggle_side_bar`)
- `ctrl+shift+b`: Build project (`build`)
- `alt+up`: `swap_line_up`
- `alt+down`: `swap_line_down`
- `shift+tab`: unindent line regardless of cursor position in line (`shift_tab_unindent` setting set to `true`)

### OSX

- `ctrl+super+g`: Select all instances of the current selection in file (`find_all_under`)
- `super+f2`: Select all instances of the current selection in file (`find_all_under`)
	+ N.B. The default keymap for Sublime Text already allows `super+d` to expand the selection to include the current selection's next occurrence.
- `super+alt+l`: Split a multi-line selection into multiple lines (`split_selection_into_lines`)
- `super+b`: Toggle the sidebar (`toggle_side_bar`)
- `super+shift+b`: Build project (`build`)
- `alt+up`: `swap_line_up`
- `alt+down`: `swap_line_down`
- `shift+tab`: unindent line regardless of cursor position in line (`shift_tab_unindent` setting set to `true`)