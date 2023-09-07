# 💩 turdmaster

Functions to delete Mac OSX filesystem turds

## Turds?

Turds are filesystem artifacts on Mac OSX that start with `._`, they are created by the OS to hold extra filesystem attributes supported by HFS+.

When moving to linux or windows, or deploying files to a server, these turds are of no value.

### `is_turd`

Checks whether a file is a turd, exits with status 0 if true or 1 if false.

### `dump_turd`

Checks whether a file is a turd and removes it if so.

### `dump_turds`

Searches a path for turds and removes them.
