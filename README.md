# Youtube-dl-mp4

This script will download the best video quality, audio quality, and a thumbnail from a 
youtube video url that you provide than combine them together using ffmpeg.
I have tested this script on some debian based operating systems with the sudo command enabled
and with my user being a part of the sudo group.

___

## Packages that are required for this script to work:
1. Prerequesetion:
	1. Python 2.x or 3.x :

			sudo apt install python
	
	2. Curl ( To download the script. ) :
	
			sudo apt install -y curl

2. youtube-dl ( To download the youtube videos. ) [youtube-dl original website](http://ytdl-org.github.io/youtube-dl/download.html):

		sudo curl -L https://yt-dl.org/downloads/latest/youtube-dl -o /usr/local/bin/youtube-dl; sudo chmod a+rx /usr/local/bin/youtube-dl

3. atomicparsley ( to combine the thumbnail into the video. ):

		sudo apt install -y atomicparsley

4. ffmpeg ( to transcode the video into mp4, the audio into mp3, and to combine them. ):

		sudo apt install -y ffmpeg

___

## How does the script work?

you will need to put this script in a folder that is listed in your PATH variable or symbolically link this script to
a folder that is listed in your PATH variable.

1. download this script to a folder and symbolically link it to a folder listed in the PATH variable( `/usr/local/bin` is probably going to be listed in your PATH variable ).

		mkdir ~/script
		wget https://raw.githubusercontent.com/diyaa59/youtube-dl-mp4/master/youtube-dl-mp4 -P ~/script
		sudo chmod 750 ~/script/youtube-dl-mp4
		sudo ln -s ~/script/youtube-dl-mp4 /usr/local/bin
		
2. just run the script and give it the URL of the video in the first argument.

		youtube-dl-mp4 <video_URL>

___