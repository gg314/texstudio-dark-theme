# TeXstudio Dark Theme
A dark Qt skin for the TeXstudio GUI and a matching syntax highlighter.

This repository includes two complimentary approaches to creating a dark theme for the TeX editor TeXstudio.
* The GUI is written with Qt, so it can be styled with a `stylesheet.qss` file. This file must be placed where TeXstudio stores its settings. It is read each time the program is started.
* The syntax highlighter settings are stored in a `.txsprofile` file. After saving your current configuration, you can load these settings through `Options > Load Profile...`.
