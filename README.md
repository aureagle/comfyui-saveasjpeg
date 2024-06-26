# ComfyUI-Saveasjpeg
Save a picture as jpeg file in Comfy + Workflow loading

## Warning: 

I'm a novice at best at coding and some of the code is pretty hacky, so this can definitely break.

Also, jpeg only supports files up to 16383 x 16383.

### Known issues:

Import of jpegfiles breaks if import a workflow that has }Prompt:{ in a Node that has dynamic wildcards disabled.


Node doesn't resize on Save - image is in there, just needs to be resized to be visible.

## Description:

This adds a custom node to save a picture as a jpeg File and also adds a script to Comfy to drag and drop generated jpegfiles into the UI to load the workflow.

I've added a compression slider and a lossy/lossless option. The compression slider is a bit misleading.

In lossless mode, it only affects the "effort" taken to compress where 100 is the smallest possible size and 1 is the biggest possible size, it's a tradeoff for saving speed.

In lossy mode, that's the other way around, where 100 is the biggest possible size with the least compression and 1 is the smallest possible size with maximum compression. 

On default it's set to lossy with a compression of 80, below are examples for that.

 

## Installation: 

Use git clone https://github.com/aureagle/ComfyUI-Saveasjpeg in your ComfyUI custom nodes directory

## Examples: 

Lossless with compression set to 100, 17069KB
https://postimg.cc/2bPkkFN9

Lossless with compression set to 10, 17059KB
https://postimg.cc/bZTwxt1d


Lossy with compression set to 100 , 5384 KB
https://postimg.cc/WFDpcYCJ


Lossy with compression set to 10, 174 KB
https://postimg.cc/VSkLDkFg


Lossy with compression set to 80 ( Default ) , 935 KB
https://postimg.cc/3yfr6QST
