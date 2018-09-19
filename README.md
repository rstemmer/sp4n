# sp4n
sp4n [spæn] - An audio player optimized for listening to audio streams. It connects to multiple streams at once and provides an overview of their meta data.

This player is optimized for listening to audio streams aka web radio.
Traditional audio players have two major drawbacks:

0. The GUI is not optimized to present the streams meta data. In many cases, they only shows the URL they play.
0. They can only connect to one stream at a time.

This is the third version of this tool, and the first one that is open source.

**Project State:** New

## Multiple streams at once

Imagine you want to listen to music of a specific genre. For example Metal.
You know three great stations.

With traditional players, you connect to the first one and recognize, that today, the only play symphonic metal. Not what you want.
Now you connect the second station. Great music appears and you stay at that stream.
Unfortunately your favorite moderator of the third stream is online and plays your favorite songs.

Wouldn't it be nice to be connected to all three stations, getting all meta data from those streams instead of only the one you are connected to.

*sp4n* Connects to all streams and provides all the meta data.
The you can select (unmute) the stream you want to listen to.
You can simply switch between those streams without waiting for buffering.

TODO: Add screenshot

## Optimized UI

Instead of traditional players, _sp4n_ provides a user interface optimized for streams.
It not only provides all meta data of all streams, it also comes with a plug-in interface to pre-process the meta data.
Each station has a different way to build the stream title string.
Usually it is _"Band Name - Song Name"_. It can also be _"Station Name: Band Name - Song Name (Moderator)"_.
You can simply write a few lines python plugin to split those name into the information you want, namely: artist name, song name, extra information 1, extra information 2.

TODO: Add screenshot

The first version used a QT4 GUI.
The second one used ncurses.
The third one will get its own text based UI implementation.
While a GUI is not very convenient for terminal users, ncurses is a conceptual overkill.
Version two is themeable. Maybe version three will be, too.

## Installation

TODO

## Usage

TODO

### Stream-List

TODO: Explain config

```ini
[Station 1]
urls = http://station.fm
parser = station.fm.py

[Station 2]
urls = http://station2.org:1337
parser = station2.py
```

### Plugins

TODO

