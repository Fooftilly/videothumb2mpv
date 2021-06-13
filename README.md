# videothumb2mpv

## What is it?
A browser userscript that will allow you to open videos in external player mpv by simply clicking on a thumbnail without loading bloated video page with web player.

## How it works?
It simply replaces video thumbnail hyperlinks on a page, changing their protocol from https:// to mpv:// and coding the original URL as base64. The result string is then passed to mpv:// URI handler as base64 string. 

## Supported resources

* YouTube
* Vimeo

Potentially it works with anything that mpv and its youtube-dl backend supports. But in order to add support for a certain website, one needs to find its DOM selector for site specific video thumnails and put it into the dictionary inside the userscript

## Prerequisites
* Any modern web browser that supports extensions 
* mpv media player

## Instructions

1. Clone this repository
1. Install userscript manager browser extension, such as [Violentmonkey](https://violentmonkey.github.io/).
1. Create script and paste contents of userscript.js from this repository
1. Make sure the userscript is enabled
1. Install mpv URL handler using the commands below

### GNU/Linux and UNIX like

```sh
$ chmod +x install.sh
$ ./install.sh
```

## Notes
Confirmed working the following setups:
* GNU/Linux with Xorg, Mozilla Firefox browser, Violentmonkey extension
