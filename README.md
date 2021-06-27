# `youtube-dl-mp4-mp3`

**This script has been tested on `Ubuntu server 20.04, 18.04, Ubuntu desktop 20.04, 18.04, Debian 10.9 (with user being added to sudo group)`**

This script will download the best quality audio, video and thumbnail, using `youtube-dl`, from a YouTube video URL that you provide; combine them together using `ffmpeg` into an mp4 video with mp3 audio and the same thumbnail as the YouTube Video provided.
___

## TLDR

`youtube-dl-mp4-mp3` + `YouTube URL` = `mp4 Video` with a YouTube thumbnail in a folder*

## Requirements

### All requirements

```bash
sudo apt install -y ffmpeg curl atomicparsley python
```

### Each project

1. [`python`](https://www.python.org/)
	
	 For `youtube-dl`

	```bash
	sudo apt install -y python
	```

2. [`curl`](https://github.com/curl/curl)
	
	To download the `youtube-dl` script.

	```bash
	sudo apt install -y curl
	```

3. [`youtube-dl`](http://ytdl-org.github.io/youtube-dl/download.html) 

	To download the youtube videos

	```bash
	sudo curl -L https://yt-dl.org/downloads/latest/youtube-dl -o /usr/local/bin/youtube-dl
	sudo chmod a+rx /usr/local/bin/youtube-dl
	```

4. [`atomicparsley`](https://github.com/wez/atomicparsley) 

	To add the thumbnail into the video.

	```bash
	sudo apt install -y atomicparsley
	```

5. [`ffmpeg`](https://github.com/FFmpeg/FFmpeg)

	To transcode the video into mp4, the audio into mp3, and to combine them
	
	```bash
	sudo apt install -y ffmpeg
	
	```
6. [`git`](https://git-scm.com/)

	To Download the script listed in this repository and to update it in case we push updates in the future

	```bash
	sudo apt install -y git
	```
___

## How to get started?

### Download and setup:

You can Download the script through the following steps:    
1. Download the script.

	```bash
	mkdir ~/script
	git clone https://github.com/diyaa59/youtube-dl-mp4-mp3.git
	cd ~/script/youtube-dl-mp4-mp3
	sudo chmod 750 ~/script/youtube-dl-mp4-mp3/youtube-dl-mp4-mp3
	```

2. Symbolically link this script into a directory that is included in your `PATH` variable
ie. `/usr/local/bin`
	
		```bash
		sudo ln -s ~/script/youtube-dl-mp4-mp3/youtube-dl-mp4-mp3 /usr/local/bin
		```

### To use the script:

Run the script and give it the required argument.

	```bash
	youtube-dl-mp4-mp3 <URL> <download option>
	```
	```txt
	<download option> can be either
	1. mp3-single : Download a single audio file out of a URL you provide even if the URL links to a playlist.
	2. mp3-list: Download a full playlist from youtube (as long as you provide the playlist URL and NOT the URL of a single video)
	3. mp4: Download a video in the highest available video quality, and the highest available audio quality.
	```
___
### To update the script:

To update the script you would need to run the following commands:

	```bash
	cd ~/script/youtube-dl-mp4-mp3
	git pull
	```