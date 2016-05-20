# node-spotify-downloader

A community driven CLI and GUI solution to download music from Spotify
[![Join the chat at https://gitter.im/Lordmau5/node-spotify-downloader](https://badges.gitter.im/Lordmau5/node-spotify-downloader.svg)](https://gitter.im/Lordmau5/node-spotify-downloader?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Download entire Spotify playlists, albums or tracks (directly from Spotify at 160kbps) to your local machine.

### Features
- ID3 tags
- Album art image
- Download entire library
- Custom folder hierarchy

### Known problems
- ID3 tags don't work with Unicode characters

### Prerequisites
- Install NodeJS **(v4.4.4 LTS)** if you haven't already. ([NodeJS Downloads](https://nodejs.org/en/))
- Download this repository as a .zip archive
- Unpack the contents to a folder of your choice
- Run `npm install` from a commandline

### CLI Usage

	Usage: node main.js [options]

	Options:

	    -h, --help                   output usage information
	    -V, --version                output the version number
	    -u, --username [username]    Spotify Username (required)
	    -p, --password [password]    Spotify Password (required)
	    -i, --uri 	   [URI / URL]   Spotify URI / URL for playlist, album or track - another valid input for this is "library"
	    -d, --directory [directory]  Download Directory - Default: "downloads" folder within the same directory
	    -f, --folder                 Create a sub-directory for playlist / album / library or specify folder hierarchy format

#### So
  If you wanted to download the playlist "Top 100 Hip-Hop Tracks on Spotify", you would use the following command:

	node main.js -u yourusername -p yourpassword -i spotify:user:spotify:playlist:06KmJWiQhL0XiV6QQAHsmw
	OR
	node main.js -u yourusername -p yourpassword -i https://play.spotify.com/user/spotify/playlist/06KmJWiQhL0XiV6QQAHsmw

  If you wanted to download the album "Epiphany", you would use the following command:

	node main.js -u yourusername -p yourpassword -i spotify:album:44Z1ZEmOyois0QoAgfUxrD
	OR
	node main.js -u yourusername -p yourpassword -i https://play.spotify.com/album/44Z1ZEmOyois0QoAgfUxrD

  If you wanted to download the track "2Pac I Get Around", you would use the following command:

	node main.js -u yourusername -p yourpassword -i spotify:track:74kHlIr01X459gqsSdNilW
	OR
	node main.js -u yourusername -p yourpassword -i https://play.spotify.com/track/74kHlIr01X459gqsSdNilW

#### Path format
If you pass `-f` flag without specifying a file path template, it will save the
songs inside a folder with the name of the album/playlist, or inside a `Library`
folder in case you are downloading all saved songs (`-i library`).

If you want to specify a path template, the following tokens are available:

- `{track.name}`
- `{artist.name}`
- `{album.name}`
- `{album.year}`

e.g. `-f "{artist.name}/{album.name} [{album.year}]/{track.name}"`
will result in: `Rammstein/Mutter [2001]/Sonne.mp3`


### Or Run it from your browser
  To open in browser, just run from terminal/cmd file run.sh/run.bat (depends of your OS)
    this file will install all needed modules an start a local server (address will be displayed in terminal, by default is http://localhost:3001).
    Just open this address in your browser and ... enjoy :)


### Disclaimer
- Don't use it ( ͡° ͜ʖ ͡°)
