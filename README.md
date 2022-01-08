# anime-terminal

A cli to browse, watch and download anime.

Watch your favorite anime from linux terminal. You don't need a browser to watch anime now.

This tool scrapes the site [gogoanime](https://gogoanime.cm).

### Dependencies
- grep
- curl
- sed
- mpv
- ffmpeg
#### Optional: vlc

# Installation
### Linux / Mac
```sh
git clone https://github.com/whoisYoges/anime-terminal
cd anime-terminal
chmod +x anime-terminal
sudo cp anime-terminal /usr/local/bin/
```
### Uninstallation
`sudo rm /usr/local/bin/anime-terminal`
### Usage
```
anime-terminal [-kv] [--dub] [-q <quality>] [-d | -p <download_dir>] [<query>]
anime-terminal [-kv] [--dub] [-q <quality>] -u | -n | -H
anime-terminal -h | -D

Options:
 -u	 shows anime from history with unwatched episodes
 -n	 show recent anime
 -h	 show this help text
 -d	 download episode
 -H	 watch from history; continue from where you left off
 -D	 delete history
 -q	 set video quality (best/worst/360/480/720/..)
 -k	 on keypress navigation (previous/next/replay/quit episode)
 -v	 use VLC as the media player
 --dub	 play the dub version if present

Episode selection:
 Add 'h' on beginning for episodes like '6.5' -> 'h6'
 
Multiple episodes can be chosen given a range
 Choose episode [1-13]: 1 6
 This would choose episodes 1 2 3 4 5 6
```
