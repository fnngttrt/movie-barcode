# THIS IS THE BETA-BRANCH
# IT IS VERY UNSTABLE
# PLEASE ONLY USE THE MASTER-BRANCH FOR OPTIMAL PERFORMANCE

# movie-barcode
A simple program to create movie-barcodes

## What are movie barcodes?
Its a technique, where every frame in a movie gets compressed into a line, giving an idea of the colour palette used by the filmmakers.
And it looks really cool!

# Example:
Standard Bar-width
![Barode with standard width](https://i.imgur.com/aqyMGzm.jpg)

Bar-width 15px
![Barcode with bar-width 15](https://i.imgur.com/qHLmMiQ.jpg)

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
-o --OUTPUT: Define the output file

-w --BARWIDTH: Sets the width of each bar in the final image (Default: 5)

--height: Sets the height of the final image (Default: same as src-video)

-i --INTERVAL: Defines the interval where the frames get picked out of the video (Default: 1000 == every Second)

--> If you use a long clip (more than 15 Minutes) i would suggest using a value around 10000

--> Otherwise the program uses too much disk-space

-v --VERBOSE: Enables verbose output
