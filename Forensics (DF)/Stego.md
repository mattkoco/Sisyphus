# Steganography 
```
- Aperisolve
- Stegosuite
- Stegcracker (or equivalent)
- binwalk
- foremost
- exiftool
```
# Commands
```
$ binwalk -e flag.png
$ strings flag.png
$ hexdump -C flag.png
```
- Use pngcheck for PNGs to check for any corruption or anomalous sections
- ***pngcheck -v***
- PNGs can contain a variety of data ‘chunks’ that are optional (non-critical) as far as rendering is concerned.

  - bKGD gives the default background color. It is intended for use when there is no better choice available, such as in standalone image viewers (but not web browsers; see below for more details)
  - cHRM gives the chromaticity coordinates of the display primaries and white point
  - gAMA specifies gamma
  - hIST can store the histogram, or total amount of each color in the image
  - iCCP is an ICC color profile
  - iTXt contains UTF-8 text, compressed or not, with an optional language tag. iTXt chunk with the keyword
  - pHYs holds the intended pixel size and/or aspect ratio of the image
  - sBIT (significant bits) indicates the color-accuracy of the source data
  - sPLT suggests a palette to use if the full range of colors is unavailable
  - sRGB indicates that the standard sRGB color space is used
  - sTER stereo-image indicator chunk for stereoscopic images
  - tEXt can store text that can be represented in ISO/IEC 8859-1, with one name=value pair for each chunk
  - tIME stores the time that the image was last changed
  - tRNS contains transparency information. For indexed images, it stores alpha channel values for one or more palette entries. For truecolor and grayscale images, it stores a single pixel value that is to be regarded as fully transparent
  - zTXt contains compressed text with the same limits as tEXt

*** Aperisolve can solve most basic Stego challenges. Stego can be much harder then what you find on sites like PicoCTF - don't assume all stego challenges are freebies. ***
