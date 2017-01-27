# What

Quotify: A python library for creating inspirational images

Creates inspiring quotes with beautiful backgrounds, like these:

<img src="https://pbs.twimg.com/media/C3M8s82WEAA1RPJ.jpg:large" />

<img src="https://pbs.twimg.com/media/C3M8sJOWcAAJetr.jpg:large" />

<img src="https://pbs.twimg.com/media/C3M8rp5XUAEDBd0.jpg:large" />

<img src="https://pbs.twimg.com/media/C3M8qYRWAAEplul.jpg:large" />

<img src="https://pbs.twimg.com/media/C3M8tTQWYAEW6ZR.jpg:large" />

# Why

To tweet out amazing quotes from <a href="https://twitter.com/startupctoio">@StartupCTOio</a>

# Running

1. Clone repo, then in shell

```
cd repo
pip install -r requirements.txt
mkdir input 
mkdir output
mkdir fonts

```

2. Populate the `input` directory with background images.

3. Populate the `fonts` directory with fonts.

4. Then, in python:

```
# text
text = "This is a test. This is a test. This is a test. This is a test. "
output_filename = "output/{}.png".format(int(time.time()))

# config
FONT = select_font()
FONT_SIZE = recommend_font_size(text)
print(FONT_SIZE)
IF = ImageFont.truetype(FONT, FONT_SIZE)
IMAGE_WIDTH = 600
IMAGE_HEIGHT = 350
COLOR = (255, 255, 255)
SPACING = 3


print(write_image(text, output_filename, background_img=select_background_image()))


```