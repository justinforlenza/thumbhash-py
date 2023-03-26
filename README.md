<img src="https://img.shields.io/pypi/v/thumbhash-py"> <img src="https://img.shields.io/github/license/justinforlenza/thumbhash-py">

# thumbhash-py
A Python port of the [thumbhash](https://github.com/evanw/thumbhash) encoder by [Evan Wallace](https://github.com/evanw)

## Installation
Install thumbhash with pip
```sh
pip install thumbhash-py
```
Optionally install with pillow support:
```sh
pip install thumbhash-py[pillow]
```

## Usage
Encode a RGBA array to a ThumbHash
```py
from thumbhash import rgba_to_thumb_hash


rgba = [100, 85, 15, 255, 100, 84, 32, 255,...]
width = 100
height = 75

thumb_hash = rgba_to_thumb_hash(rgba, width, height) # [86, 8, 10, 13, 128, 22, 234, 86, 111, 117, ...]
```
Open an image using pillow, scale down to max dimensions of 100x100 and encode to a ThumbHash
```py
from thumbhash import image_to_thumb_hash

thumb_hash = image_to_thumb_hash('image.jpg') # [86, 8, 10, 13, 128, 22, 234, 86, 111, 117, ...]
```

## Features
As of now this library only handles the conversion of images to hashes, not the reverse.
