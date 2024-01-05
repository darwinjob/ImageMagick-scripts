# ImageMagick-scripts
ImageMagick scripts for converting image folders.
## System requirements
The scripts require ImageMagick 7 to be intalled on you Windows machine. Download and install ImageMagick here https://imagemagick.org/script/download.php#windows The version "Win64 static at 16 bits-per-pixel component" is recommended.
## Check if ImageMagick 7 is installed on your computer
Run CMD, at the prompt type `magick.exe -version`. You should see the output similar to this one:
```
C:\>magick.exe -version
Version: ImageMagick 7.0.6-0 Q16 x64 2017-06-11 http://www.imagemagick.org
Copyright: Copyright (C) 1999-2015 ImageMagick Studio LLC
License: http://www.imagemagick.org/script/license.php
Visual C++: 180040629
Features: Cipher DPC HDRI
Delegates (built-in): bzlib cairo flif freetype jng jp2 jpeg lcms lqr openexr pa
ngocairo png ps rsvg tiff webp xml zlib
```
If you don't see the output ImageMagick is not (proprely) installed.
## How to use scripts
Download and unzip https://github.com/darwinjob/ImageMagick-scripts/releases/download/v1.0/scripts.zip into a folder of your choice e.g. "scripts". All the scripts use the same syntax:
```
script_name.bat inputfolder outputfolder
```
where `inputfolder` is the folder containing images to be processed, `outputfolder` is the folder where processed images will be stored.
> [!WARNING]
> Both `inputfolder` and `outputfolder` must exist **before* you run a script.

> [!CAUTION]
> `inputfolder` and `outputfolder` must not be the same folder!
### Example
In most of the cases the script names are self-explanatory. Let's take `tif_to_tif_lzw_256tiled.bat` script as the example. This script will process all `.tif` files in `c:\inputfolder`, convert them to LZW compressed tiled (tile size is 256x256 pixels) TIFFs and store the result in `c:\outputfolder` using the same filenames as the originals. Run CMD, go to your script folder and type:
```
C:\scripts>tif_to_tif_lzw_256tiled.bat c:\inputfolder c:\outputfolder
```
### Scripts
`jp2_to_tif_lzw_256tiled.bat` - .jp2 files to LZW compressed tiled (tile size is 256x256 pixels) TIFFs  
`jpg_to_tif_lzw_256tiled.bat` - .jpg files to LZW compressed tiled (tile size is 256x256 pixels) TIFFs  
`jpg_to_tif_resizeParameter_lzw_256tiled.bat` - .jpg to LZW compressed tiled (tile size is 256x256 pixels) resized TIFFs  
`png_to_png_truecolor8bit.bat` - .png files to RGB (no transparency) PNGs  
`png_to_tif_lzw.bat` - .png to LZW compressed untiled TIFFs  
`tif_to_png.bat` - .tif to PNGs  
`tif_to_tif64_lzw_256tiled.bat` - .tif to LZW compressed tiled (tile size is 256x256 pixels) BigTIFFs  
`tif_to_tif_jpg_256tiled.bat` - .tif to JPEG compressed tiled (tile size is 256x256 pixels) TIFFs  
`tif_to_tif_jpg_75q_256tiled.bat` - .tif to JPEG compressed tiled (tile size is 256x256 pixels) TIFFs, JPEG compression quality is 75  
`tif_to_tif_lzw_256tiled.bat` - .tif to LZW compressed tiled (tile size is 256x256 pixels) TIFFs  
`tif_to_tif_lzw_256tiled_spaces_in_filenames.bat` - .tif to LZW compressed tiled (tile size is 256x256 pixels) TIFFs, should tolerate spaces in filenames  
`tif_to_tif_normalized_lzw_256tiled.bat` - .tif to LZW compressed tiled (tile size is 256x256 pixels) normalized TIFFs
`tif_to_tif_resizeParameter.bat` - .tif to resized TIFFs  
`tif_to_tif_truecolor8bit_lzw_256tiled.bat` - .tif to LZW compressed tiled (tile size is 256x256 pixels) RGB (no transparency) TIFFs
`tif_to_tif_truecolor8bit_normalized_lzw_256tiled.bat` - .tif to LZW compressed tiled (tile size is 256x256 pixels) RGB (no transparency) normalized TIFFs
`tif_to_tif_uncompressed_256tiled.bat` - .tif to uncompressed tiled (tile size is 256x256 pixels) TIFFs  

### Helper tool
ImageMagickGUI.exe
### Validadtor
### Replace spaces and minuses in filenames
