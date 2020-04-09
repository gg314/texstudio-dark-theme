# TeXstudio Dark Theme
This repository includes two complimentary approaches to creating a dark theme for the TeX editor TeXstudio.
* The GUI is written with Qt, so it can be styled with a `stylesheet.qss` file. This file must be copied to the TeXstudio settings directory (see below).
* The syntax highlighter settings are stored in `texstudio.ini`. You will need to manually copy lines into your settings file (or choose your own syntax colors).
* The UI and syntax highlighting here are pretty clearly inspired by the default settings for VSCode.
* The results here are not quite polished or professional, but they might serve as a launching point for a better dark theme. For example, Qt should allow for replacing many of the UI symbols with dark-theme compatible images.

## Preview
<img src="docs/preview.png" />

## How to use
### Qt GUI
To override Qt GUI settings, TeXstudio allows for a `stylesheet.qss` file that is automatically loaded at program startup. The file needs to be copied to the correct directory:
* [TeXstudio: Where are the settings stored?](https://github.com/texstudio-org/texstudio/wiki/Frequently-Asked-Questions#where-are-the-settings-stored)
* **Linux/Unix/Mac**: `~/.config/texstudio/texstudio.ini`
* **Windows**: `%APPDATA%\texstudio\texstudio.ini`
* **Portable**: `config/texstudio.ini` relative to the TeXstudio executable

### Syntax highlighting
Syntax highlighting settings are stored with other settings in `texstudio.ini`. **You probably do not want to replace all settings** because they include default paths to a PDF viewer and other programs. To include syntax highlighting, make a backup and then manually copy the `[formats]` section (around line 400 and below) to replace the corresponding section of your own `texstudio.ini`. See above for the location of this file. Colors can be changed later at <kbd>Options | Configure TeXstudio</kbd> under <kbd>Syntax Highlighting</kbd>.

*Note*: Close TeXstudio before editing `texstudio.ini`. When TeXstudio is closed, any edits in `texstudio.ini` will be overwritten.


### Other options
You may wish to change the default internal PDF viewer paper color and highlight color. These can be found through <kbd>Options | Configure TeXstudio</kbd>; check <kbd>Show Advanced Options</kbd>, and then make edits under <kbd>Internal PDF Viewer | Paper Color</kbd>.