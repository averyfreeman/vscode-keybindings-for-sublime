# VS Code keymaps for Sublime Text 3

---

#### Part one of my on-going text-editor series:

#### "Change is hard! For the love of god, please make it stop!"

(part two)[https://github.com/averyfreeman/vscode-windows-keybindings-for-linux-users]

Everyone has a particular kinetic motion they are used to, speaks to them, makes them feel comfortable, and gives them that warm, fuzzy feeling akin to a Courvoisier in front of a fire on a bear skin rug at a ski resort in the Swiss Alps. Like they're one with their keyboard - the distance between them and their keyboard disappears with their choice, and they are less human being than a borg fully assimilated, the clack sounding more heroically amiable than Sir Patrick Stewart after an epically first-rate fluffing. 

For some it's vim (I'm 1/2 in that camp), for some it's Sublime, for some it's `edit.exe` in MS DOS 6.2 (remember those days?). They're all great choices I can completely understand. But for me, it's the VS Code keymap in Windows.  Don't ask me why, because I couldn't tell you, but for some reason it just speaks to me personally.  It *feels right*.  Maybe it's familiarity, muscle memory, etc. but it also just seems like a great layout for my stubby little fingers and neural carvasses of my syphillitic grey matter. 

But even though I absolutely love its key layout, I don't always want to have to *open* VS code. I use [VS Code](https://code.visualstudio.com/) for coding. I've tried using it for text editing a bit, but my installation is too heavy. With as many extensions as I run, it can't be considered "light" anymore, and certainly not light enough for simple text editing duties.

Therefore, I started using [Sublime Text](https://www.sublimetext.com) for notes, markdown, and config files. It's the ultimate replacement for `notepad.exe` if you're into coding. If you're used to something between a text editor and an IDE, it really is ideal when necessitating minimal amounts of plugins. It's more than tolerable to use right out of the box, it has tab size control, extensibility, configuration with JSON files (what uber-nerd out there doesn't love that?) ... 

... but most of all, I love that I can edit its keybindings to feel almost just like VS Code for Windows. Now THAT is amazing. Maybe not to some people, but to me it's like heaven. So, this fork is an attempt to make Sublime feel as much like VS Code as possible without becoming a cumbersome, slow-loading semi-IDE, repleat with unnecessary bloat for simple duties. Svelte like a summer swimmer in the sun of the Sahara. Sometimes it's hard to believe we've come so far... 

There are a lot of [Sublime-to-VSCode keymaps](https://marketplace.visualstudio.com/items?itemName=ms-vscode.sublime-keybindings) out there, but precious few **VS Code for Sublime** keymaps. Thankfully I found *one* from [JennyNZ](https://github.com/jennynz/vscode-keybindings-for-sublime), forked and updated by [yasapurnama](https://github.com/yasapurnama/vscode-keybindings-for-sublime) that I find quite amenable.

JennyNZ actually did an amazing write-up about her note-taking workflow, which I've included at the end of this readme, as well.  I must assert that it is hers and not mine, because trust me, I can take no credit for a piece of work that well calculated, it'd scream plagurism loudly enough to beggar belief.

- [Compare](<(https://github.com/jennynz/vscode-keybindings-for-sublime/compare/master...yasapurnama:master)>)

Unlike previous renditions, my goal with these keymaps is slightly different: I plan to make them *all* just like Windows, because I have absolutely no interest in changing behaviors for different platforms - if I can bend *all* of the platforms to *my* threadbare kinetic familiarity like a maleable playdough on a hot summer morning, I will have actualized my true life's calling of being comfortable typing all of the time.

Note:  As of 2021-12-19, I have not updated any of the Mac OS keybindings yet, as I am still working on getting my Big Sur VM back up and running.

The easiest way to implement these kebindings is to:
 - 1. Navigate to the file on this repo page that correponds to your OS
 - 2. Hit "raw", copy the page and paste it into the window on the right in `Preferences => Keybindings` menu in Sublime Text
(I recommend not editing the default settings on the left)

You can grab my preferences, too, if you like. These are added in the same way as keybindings, but under `Preferences => Settings`

JennyNZ said she uses the [Zettelklasten method](https://zettelkasten.de/) for note-taking, which looks very interesting - I recommend checking it out, as it's quite comprehensive.

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
  - N.B. The default keymap for Sublime Text already allows `ctrl+d` to expand the selection to include the current selection's next occurrence.
- `alt+shift+i`: Split a multi-line selection into multiple lines (`split_selection_into_lines`)
- `ctrl+b`: Toggle the sidebar (`toggle_side_bar`)
- `ctrl+shift+b`: Build project (`build`)
- `alt+up`: `swap_line_up`
- `alt+down`: `swap_line_down`
- `shift+tab`: unindent line regardless of cursor position in line (`shift_tab_unindent` setting set to `true`)

### OSX

- `ctrl+super+g`: Select all instances of the current selection in file (`find_all_under`)
- `super+f2`: Select all instances of the current selection in file (`find_all_under`)
  - N.B. The default keymap for Sublime Text already allows `super+d` to expand the selection to include the current selection's next occurrence.
- `super+alt+l`: Split a multi-line selection into multiple lines (`split_selection_into_lines`)
- `super+b`: Toggle the sidebar (`toggle_side_bar`)
- `super+shift+b`: Build project (`build`)
- `alt+up`: `swap_line_up`
- `alt+down`: `swap_line_down`
- `shift+tab`: unindent line regardless of cursor position in line (`shift_tab_unindent` setting set to `true`)
