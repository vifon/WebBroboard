# WebBroboard

**WebBro**wser + clip**board** = **WebBroboard**

## Why?

### The problem

I tend to use many browsers or browser settings for different links. I
prefer to launch some links in the private mode, some in the regular
mode, some in a different browser profile (they are pretty handy in
Chromium, try them out!). Until now I used to right-click and copy to
clipboard most links in the external applications (like Thunderbird)
to open them manually in whichever way I prefer. It was tedious and
didn't help when the application launched some site by itself
(example: pressing F1 in Thunderbird).

### The solution

What if my clipboard *was* my web browser? Clicking a link would only
copy it to my clipboard and then display an unobtrusive notification.
This is exactly what *WebBroboard* is, a wrapper around `xsel(1)` and
`notify-send(1)` + a `.desktop` file to hook it up as a browser.

## How?

To use WebBroboard, copy the `webbroboard` file into a directory in
your PATH and copy `webbroboard.desktop` into
`~/.local/share/applications`. Then run the following commands to set
it as your default web browser:

```bash
xdg-mime default webbroboard.desktop x-scheme-handler/https
xdg-mime default webbroboard.desktop x-scheme-handler/http
xdg-mime default webbroboard.desktop text/html
```

Dependencies:

- xsel(1)
- notify-send(1)
- Bash

Enjoy!

## Who?

Copyright (C) 2017  Wojciech Siewierski < wojciech dot siewierski at onet dot pl >

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
