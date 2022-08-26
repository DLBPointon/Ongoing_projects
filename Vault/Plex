# Plex Installation

Roughly followed this tutorial: https://www.wundertech.net/how-to-install-plex-on-openmediavault/

## Issues so far:

The first time I set up plex I loaded all media as movies so my library was a complete mess.

This time I'm planning to do things propperly so set up a TV show library for by Stargate library.

Only 6 episodes across 5 seasons showed up, mind you there are 221 episodes across 10 seasons.

It turns out that Plex requires a certain format for the file name to be ingested correctly.

`show/season/show-episode-episodename.ext` not `show/season/show[episode]episodename.ext`

Minor, but Plex cares and after realising how long this would take changing the files manually I made a python script to do it for me (Bash would throw too many errors).

```python
import re
import os

for i in os.listdir():
    new = re.sub(' \[|\] ', '-', i)
    print(f'{i}{\t\t} -> {new})
    os.rename(i, new)
```

This has to be run in each folder individually, for some issue it couldn't find all files if run in the root folder (because of spaces I think).
