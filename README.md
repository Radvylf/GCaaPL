# Google Chrome as a Programming Language

Originated from a [discussion](https://chat.stackexchange.com/transcript/message/57536756#57536756) in The Nineteenth Byte. This is a formal specification for the usage of Google Chrome as a Programming Language.

## Interpreter

Any version of Google Chrome should work as an interpreter, as long as it has support for the features mentioned here. JavaScript must be enabled for any sites being used in the program (the one used here is `https://amidst.dev/_/*`), along with pop-ups. These can be ignored for kolmogorov complexity challenges in which only basic keystrokes are used and no webpages need to open or close tabs.

## Usage

To interpret a GCaaPL program, take the contents of the program. Starting with a single chrome window open to `about:blank` (in addition to input), input all keystrokes in the correct order, waiting for any actions to finish if this is necessary. This includes pages loading, and tabs opening or closing. Once all keystrokes have been inputted, if all windows have not yet been closed, input should restart from the beginning. Once all windows opened by the program have been closed (including the initial tab), the program is done.

## Keystrokes

A GCaaPL program is made up of keystrokes. It is assumed that all printable ASCII characters can be typed on the keyboard, with the standard US layout and shortcuts, but no assumptions about the OS may be made (including behavior of any `alt` or `meta` keystrokes).

## Input/Output

Input and output should be taken in unary, as a positive integer. Input is represented by appending that many `about:blank` tabs to the initial tab, and output is taken by counting the number of open tabs when the window was closed and decrementing it (to account for the initial tab).

## Tips

The following keystrokes can be useful:

- `ctrl + w`: close the current tab, returning to the previously one
- `ctrl + r`: reload the current tab (useful for re-running JS scripts)
- `ctrl + t`: open a new tab
- `ctrl + shift + t`: reopen last closed tab (or window)
- `ctrl + _`: (where `_` is a number `1` to `8`) switch to `n`th tab
- `ctrl + 9`: switch to final tab
- `ctrl + l`: focus the address bar
- `ctrl + n`: new window
- `ctrl + shift + w`: close window
- `ctrl + tab`: next tab
- `ctrl + shift + tab`: previous tab

At `https://amidst.dev/_/`, there is a script which opens a single new tab on page load and focuses it.
