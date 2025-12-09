# VidSnapAI

So basically I got tired of spending hours editing short videos and thought "there's gotta be a better way to do this." This is what I came up with.

## What it does

Takes your video clips and text, generates a voiceover, and stitches everything together. Made it for creating reels/shorts without having to mess around in Premiere or CapCut for an hour.

The whole thing runs through a web interface so you don't have to deal with command line stuff if you don't want to.

## Setup

You'll need Python and FFmpeg installed. If you don't have FFmpeg, google "install ffmpeg" + your OS.

```bash
git clone https://github.com/Harshits9/VidSnapAI.git
cd VidSnapAI
pip install -r requirements.txt  # might need to make this file first
```

Add any API keys you need to `config.py`. Then just run:

```bash
python main.py
```

Should open up on localhost:5000 or it'll tell you the port in the terminal.

## How to use

1. Upload your video/images
2. Type out what you want the voiceover to say
3. Hit generate
4. Download the result

Pretty straightforward.

## File structure

```
main.py              - flask app
generate_process.py  - handles the video generation
text_to_audio.py     - TTS stuff
config.py            - put your api keys here
templates/           - html files
static/              - css/js
user_uploads/        - where uploads go
```

## Issues

If it's slow, your video is probably too big. Try compressing it first.

If the voice sounds weird, check your API key in config.py.

If something else breaks, check the terminal output - usually tells you what went wrong.

## Todo

- add more voice options
- batch processing would be nice
- maybe add some templates
- better error handling

Feel free to contribute if you want to add something.
