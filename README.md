# anime-terminal

A cli to browse, watch and download anime.

Watch your favorite anime from *nix terminal. You don't need a browser to watch anime now.

This tool scrapes the site [gogoanime](https://gogoanime.cm).
### Dependencies
- grep
- curl
- sed
- mpv
- openssl
- aria2 (Only for downloading)
- ffmpeg (Only for downloading)

*Most of the latest anime episodes are available only in m3u8 format which cannot be downloaded by aria2, so using ffmpeg instead. It isn't required for streaming though!'*

# Installation
**Make sure you've installed all the dependencies on your system.**
```
git clone https://github.com/whoisYoges/anime-terminal
cd anime-terminal
chmod +x anime-terminal
sudo cp anime-terminal /usr/local/bin/
cd ..
rm -r anime-terminal
```
### Uninstallation
```
sudo rm /usr/local/bin/anime-terminal
```
### Usage
```
Usage:
    anime-terminal [-q <quality>] [-a <episode>] [-d | -p <download_dir>] [<query>]
    anime-terminal [-q <quality>] -c
    anime-terminal -h | -D 
Options:
    -c continue watching anime from history
    -a specify episode to watch
    -h show helptext
    -d download episode
    -p download episode to specified directory
    -q set video quality (best|worst|360|480|720|1080)
    -D delete history
Episode selection:
    Add 'h' on beginning for episodes like '6.5' -> 'h6'
    Multiple episodes can be chosen given a range
    Choose episode [1-13]: 1 6
        This would choose episodes 1 2 3 4 5 6
	To select the last episode use -1

    When selecting non-interactively, the first result will be
    selected, if anime is passed
```
