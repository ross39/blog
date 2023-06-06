---
layout: post
title: Video Compression Basics
---
In this blog post I will attempt to explain video compression basics. Video compression is a vast topic and clearly one blog post is not 
even going to scratch the surface. Instead my aim will be to explain, as best I can, video compression basics as it relates to my MSc thesis
which is currently ongoing. I will include links to references used so that the reader can check out those resources for themselves. 

❗️I profess no expertise in this area. I am simply a curious developer who enjoys technical challenges and if any meaningful work arises 
out of this then so be it. This is MSc thesis is a work in progress and as such, ideas are likely to change. I do not claim authority and any
explainations given here are given with the caveat that I could be wrong😱. 

Lets with general compression before we move onto video compression. Compression is used everwhere, so much so its hard to name an area where 
compression is not used. The main idea around compression is that we want to store information using as few bits as possible. If you have ever used 
those button phones from the early 00s, people invented all sorts of texting abbreviations to shorten the number of button presses needed to send a 
text message. This is a form of compression. Now in 2023, compression is universally used to compress everything from images, audio, video, games and 
basically anything that can be stored digitally. In Ireland, the average wi-fi speed ranges from 24-100 mbps. If you wanted to watch a 1080p movie from 
Netflix without compression, you would need a wi-fi speed of approximately 3000mbps. 1080p has an uncompressed bitrate of approximately 3GBps while 4k video
has an uncompressed bitrate of 12GBps. Yikes

There are two types of compression. Lossless and lossy. Video streaming is nearly always lossy whilst stuff such as zip files, pdf files etc are lossless. 
This is because you are less likely to notice a few missing pixels from a Netflix movie than if your pdf document is missing words and sentences. Huffman Encoding 
is a lossless, entropy-based, compression algorithm that was proposed in 1952. It is still used in JPEG and ZIP file formats. Runlength encoding is a fast, lossless
compression algorithm which was proposed in 1959. It is still used today in PDF and TIFF files. H.264 is a video compression codec standard. 
It is ubiquitous - internet video, Blu-ray, phones, security cameras, drones, everything. Everything uses H.264 now. It is a lossy compression with a single goal in mind.
To reduce the bandwidth required for transmission of full-motion video.

But wait! I thought your idea was to use Bloom Filters for lossless video compression? (read my previous blog post). Why then does everything use lossy H.264?
H.264 uses lossy for two main reasons. Speed and compression ratio. Lossy is generally faster and achieves better compression, at the cost of throwing away information, than lossless and when you're playing video, 
the person is almost guaranteed to not notice a few missing pixels and some blurred edges. However lossless video compression is also desirable for dealing with archived video or if you just want to store video
in a compressed state without suffering from compressed artifacts(blurred edges, missing pixels etc). 

So how is video compressed then? Great question. For lossy compression, Generally it involves predicting where objects will appear on the screen and making guesstimates
based on this. We might merge pixels together based on how similar they are etc. I plan to upload another blog explaining this prediction stuff in more detail.
But if you're new to compression there should be enough information here to get you started. 

[Nice overview of algorithms used in compression](https://go-compression.github.io/algorithms/overview/).
