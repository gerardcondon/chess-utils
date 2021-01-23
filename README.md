# chess-utils
Python Chess Utils for PGN files

## TODO
### Lichess Downloader Utility
* Download a user's games from Lichess
* Download games between date ranges - could use months/years here. Giving just a start date would download to the current month.
* Games should be outputted to a folder with separate pgn files for each month. Can have combined pgn files for years and overall.
* Should provide support for an update option which will just download the new games.
* Assume that any existing folders in that date format containing pgn games are complete except for the last one which could still be in progress
* Could store username etc in a config file so that we wouldn't need to keep entering it
* Investigate Lichess authentication mechanisms - can we get a key or login to avoid throttling by the API.
  - it looks like we can generate a token for ourselves [here]. We cna use this in the program. If a token is specified in the config or command line then use it. Otherwise use the non authenticated mode.
* Investigate what headers are available - do we get automatic ECO classification from Lichess or do we need to do it ourselves?
* Investigate what options are available for annotation - could store these in the config file also so that they do not need to be re-entered and we stay consistent.
* There are unofficial libraries for accessing lichess in Python. Do we want to use these? It saves us writing our own but it is an additional dependency. Leaning towards just using the bare requests library.
