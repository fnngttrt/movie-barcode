# movie-barcode
A simple program to create movie-barcodes

### Table of contents
#### 1. Explanation
#### 2. Usage
#### 3. Optional Arguments
#### 4. Examples
#### 5. Common errors

## What are movie barcodes?
Its a technique, where every frame in a movie gets compressed into a line, giving an idea of the colour palette used by the filmmakers.
And it looks really cool!

## Installation
```
git clone https://github.com/therealhe1ko/movie-barcode/
cd movie-barcode/
sudo pip3 install -r requirements.txt
./barcode.py OPTIONS
```
## Usage
./barcode.py -s SOURCE 

### Optional Arguments
```
-o --OUTPUT: Define the output file

-w --BARWIDTH: Sets the width of each bar in the final image (Default: 5)

--avg: Uses the avg color of each frame, instead of a compressed version of the image. (Default: False)

--height: Sets the height of the final image (Default: same as src-video)

-i --INTERVAL: Defines the interval where the frames get picked out of the video (Default: 1000 == every Second)

--> If you use a long clip (more than 15 Minutes) i would suggest using a value around 10000

--> Otherwise the program uses too much disk-space

-v --VERBOSE: Enables verbose output
```


### Examples:

default result from a 240s clip
![Barcode with standard bar-width](https://i.imgur.com/wXbW3QX.jpg)

--avg result from same clip
![Barcode with --avg parameter](https://i.imgur.com/Nl2Ut2u.jpg)


### Errors:

#### I'm getting this warning:

``` [h264 @ 0x2557340] mmco: unref short failure ```

This comes from ffmpeg, but its not critical. Theres no fix currently