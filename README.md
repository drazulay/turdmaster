# 💩 turdmaster

Functions to delete Mac OSX filesystem turds

## Turds?

Turds are filesystem artifacts on Mac OSX that start with `._`, they are created by the OS to hold extra filesystem attributes supported by HFS+.

When moving to linux or windows, or deploying files to a server, these turds are of no value.

### `is_turd`

Checks whether a file is a turd, exits with status 0 if true or 1 if false.

It does this not by checking whether the file extension starts with `._` but by checking if the if the first 16 file header bytes translate to the hexadecimal string `00051607000200004d6163204f532058`.

### `dump_turd`

Checks whether a file is a turd and removes it if so.

### `dump_turds`

Searches a path for turds and removes them.
