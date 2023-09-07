# 💩 turdmaster

Functions to delete Mac OSX filesystem turds

## Turds?

Turds are filesystem artifacts on Mac OSX that start with `._`, they are created by the OS to hold extra filesystem attributes supported by HFS+.

When moving to linux or windows, or deploying files to a server, these turds are of no value.

### `is_turd`

Checks whether a file is a turd, exits with status 0 if true or 1 if false.

It does this not by checking whether the file extension starts with `._` but by checking the file header bytes againt the hexadecimal string `00051607000200004d6163204f53205820202020202020200002000000090000003200000eb00000000200000ee20000011e0000000000000000000000000000000000000000000000000000000000000000000041545452`.

### `dump_turd`

Checks whether a file is a turd and removes it if so.

### `dump_turds`

Searches a path for turds and removes them.
