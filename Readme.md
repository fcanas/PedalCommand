# PedalCommand

Control actions from a MIDI footpedal board.

## Components

### `Command`

Command is the primary patch. Open this to run.

### `msgchange`

Accepts a pair of numbers and forwards them to its
outputs if either is different from the previously
received number in that input.

### `path_finder`

Constructs a path to media in the Media directory based
on a page directory and a file name.

### `PedalMux`

Accepts various note, program change, and control midi
messages from *my* pedal board and outputs the pedal
number, page, and control values on separate channels.
It encodes the peculiarities of how my pedal board is
set up.

### `Player`

Takes a path to an aiff file and plays it. It abstracts
over `readsf~`, eliminating the need to load the media
before starting playback.
