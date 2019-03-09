# MIX SPLITTER
Download all the songs in a youtube mix using
a console script.  

This script reads the songs in the description or a source and downloads them separetely using youtube-dl.  
## Prerequisites
Since this script uses youtube-dl we need to install some of its dependencies.

`sudo apt-get install ffmpeg`  
`sudo apt-get install atomicparsley`

This script also requires:
* Python 3
* Pip 3

## Installation
If you want to use the script globally, make sure
you're not inside a virtual environment

`pip3 install mix-splitter`

Type `mix_splitter`  in the console  
If that worked you should see this:  

> usage: mix_splitter.py [-h] -u URL [-l LOCATION] [-a ARTIST] [-s SOURCE]
mix_splitter.py: error: the following arguments are required: -u/--url

If you don't see that, you need to do the following step: 


##### Add ~/.local/bin to $PATH 
1. Open bash_profile  
`sudo nano ~/.bash_profile`
2. Paste this at the end of the file  
`export PATH=$PATH:~/.local/bin`
3. Restart the terminal  


## Usage

#### Basic
`mix_splitter -u <YOUTUBE_MIX_URL>`  
That will dowload the songs in the current directory
---

#### If you want specify the directory where the songs are downloaded
with `-l`  
`mix_splitter -u <YOUTUBE_MIX_URL> -l /directory/to/download/the_songs`

---
#### Specify album artist
Sometimes the mixes' description just contain the title of the songs (with no artist). This is usually an artist's album. To download these kind of mixes, you can specify the name of the artist with `-a`.

`mix_splitter -u <YOUTUBE_MIX_URL> -a <ARTIST>`


## What mixes are compatible?
Those that have the songs in the description.

Sometimes the mixes don't contain the song titles in the description, but they're provided in the comments.

In a case like that, copy the entire comment and paste it in a new .txt file.

Then execute the script with the command `-s` and append the path of that .txt file.

`mix_splitter -u <YOUTUBE_MIX_URL> -s /file/that/contains/the_songs.txt`



## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details











 