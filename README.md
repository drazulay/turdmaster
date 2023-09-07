# 💩 turdmaster

Functions to delete Mac OSX filesystem turds

## What are Mac OSX filesystem turds?

Turds are filesystem artefacts on Mac OSX that start with `.` and are created by the OS to hold extra filesystem attributes supported by HFS+ or other OSX-specific metadata.

Specifically, they are the files:

- `.DocumentRevisions-V100`;
- `.Spotlight-V100`;
- `.TemporaryItems`;
- `.Trashes`;
- `.fseventsd`;
- Any file that starts with `._` and of which the first 16 header bytes translate to the hexadecimal string `00051607000200004d6163204f532058`.

When moving to linux or windows, or deploying files to a server, these *turds* are of no value.

### `is_turd`

Checks whether a file is a turd and exits with status 0 if true or 1 if false (for use in pipe).

### `dump_turd`

Checks whether a file is a turd and removes it if so.

### `dump_turds`

Searches a path for turds and removes them.
