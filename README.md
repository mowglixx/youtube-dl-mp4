# `youtube-dl-mp4`

**This script has been tested on `Debian 10`**

This script will download the best quality audio, video and thumbnail, using `youtube-dl`, from a YouTube video URL that you provide; combine them together using `ffmpeg` into an mp4 video with mp3 audio and the same thumbnail as the YouTube Video provided.

## TLDR

`youtube-dl-mp4` + `YouTube URL` = `mp4 Video` with a YouTube thumbnail in a folder*

## Requirements

### All requirements

```sh
sudo apt install -y ffmpeg curl atomicparsley python
```

### Each project

1. [`python`](https://www.python.org/)

	For `youtube-dl`

	```sh
	sudo apt install -y python
	```

2. [`curl`](https://github.com/curl/curl)

	To download the script.

	```sh
	sudo apt install -y curl
	```

3. [`youtube-dl`](http://ytdl-org.github.io/youtube-dl/download.html) 

	To download the youtube videos

	```sh
	sudo curl -L https://yt-dl.org/downloads/latest/youtube-dl -o /usr/local/bin/youtube-dl
	sudo chmod a+rx /usr/local/bin/youtube-dl
	```

4. [`atomicparsley`](https://github.com/wez/atomicparsley) 

	To add the thumbnail into the video.

	```sh
	sudo apt install -y atomicparsley
	```

5. [`ffmpeg`](https://github.com/FFmpeg/FFmpeg)

	To transcode the video into mp4, the audio into mp3, and to combine them
	
	```sh
	sudo apt install -y ffmpeg
	```

## How does the script work?

You can either:    
1. Put this script in a folder that is included your `PATH`
	- Download the script and set permissions
		
		```sh
		mkdir ~/script
		
		sudo curl -L https://raw.githubusercontent.com/diyaa59/youtube-dl-mp4/master/youtube-dl-mp4 -o ~/script/youtube-dl-mp4

		sudo chmod 750 ~/script/youtube-dl-mp4
		```

2. Symlink this script into a folder that is included your `PATH`
ie. `/usr/local/bin`
	- Symlink the script to `/usr/local/bin` so it is included in the `PATH` variable
	
		```sh
		sudo ln -s ~/script/youtube-dl-mp4 /usr/local/bin
		```
		
3. Run the script and give it a URL of a video as the first argument.

	```sh
	youtube-dl-mp4 https://www.youtube.com/watch?v=dQw4w9WgXcQ
	```

___
