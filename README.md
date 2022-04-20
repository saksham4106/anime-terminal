# anime-terminal

A cli to browse, stream/watch and download anime.

Watch your favorite anime from linux terminal. You don't need a browser to watch anime now.

This tool scrapes the site [gogoanime](https://gogoanime.fi/).
### Dependencies
- grep
- curl
- sed
- mpv
- openssl

*Most of the latest anime episodes are available only in m3u8 format which cannot be downloaded by aria2, so using ffmpeg instead. It isn't required for streaming though!'*

### Optional Dependencies
- aria2 (Only for downloading; when used with -d/-p options)
- ffmpeg (Only for downloading; when used with -d/-p options)
- vlc (only required when used with -v option)

# Installation
**Make sure you've installed all the dependencies on your system.**
```
curl "https://raw.githubusercontent.com/whoisYoges/anime-terminal/master/anime-terminal" > anime-terminal
chmod +x anime-terminal
sudo mv anime-terminal /usr/local/bin/
```
### Documentation (Man Page)
Install if you need documentation (man page) for anime-terminal.
```
curl "https://raw.githubusercontent.com/whoisYoges/anime-terminal/master/anime-terminal.1" > anime-terminal.1
sudo mv anime-terminal.1 /usr/share/man/man1/
```
# Uninstallation
```
sudo rm /usr/local/bin/anime-terminal
```
### Uninstall documentation (man page) if you've installed it.
```
sudo rm /usr/share/man/man1/anime-terminal.1
```
### Usage
```
Usage:
    anime-terminal [-v] [-q <quality>] [-a <episode>] [-d | -p <download_dir>] [<query>]
    anime-terminal [-v] [-q <quality>] -c
    anime-terminal -h | -D 
Options:
    -c continue watching anime from history
    -a specify episode to watch
    -h show help text
    -d download episode
    -p download episode to specified directory
    -q set video quality (best|worst|360|480|720|1080)
    -v use vlc as video player
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
