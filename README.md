# youtube-audio-server 
Easily stream YouTube audio.

[![Build Status](https://travis-ci.org/codealchemist/youtube-audio-server.svg?branch=master)](https://travis-ci.org/codealchemist/youtube-audio-server)

## Install
`npm install -g youtube-audio-server`


## Run
`yas`


## Change port
Default port is 80.

You can easily change it by starting the server like:

`PORT=8080 yas`


## Usage
Just hit the server passing a YouTube video id, like:

http://yourServerAddress:port/[videoId]

For example:

http://10.1.2.27:4000/HQmmM_qwG4k

This will stream the requested video's audio.

You can play it on an HTML5 audio tag or however you like.


## Download audio
**YAS** can also be used to directly download audio if you pass a video id as argument.

When run in this mode, the server is not started.

**Usage:**

`yas --video [youtube-video-id] [--file [./sample.mp3]]`

**Examples:**
```
yas --video 2zYDMN4h2hY --file ~/Downloads/Music/sample.mp3
yas --video 2zYDMN4h2hY
```

**NOTE:** 

FILE defaults to `./youtube-audio.mp3` when not set.

**Alternative method:**

If you have a server instance running and you want to use it to download audio,
you can do this:

`curl [your-server-url]/[youtube-video-id] > sample.mp3`


## About dependencies
The key dependency for *youtube-audio-server* is 
[youtube-audio-stream](https://github.com/JamesKyburz/youtube-audio-stream), 
which depends on `ffmpeg`, which must be installed at system level, it's not
a node dependency!


## Install ffmpeg on OSX

`brew install ffmpeg`


## Install ffmpeg on Debian Linux

`sudo apt-get install ffmpeg`


## Testing
Just open the URL of your server instance without specifing a video id.

This will load a test page with an HTML5 audio element that will stream a test video id.


Enjoy!
# audioserver
