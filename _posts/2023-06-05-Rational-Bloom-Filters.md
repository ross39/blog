---
layout: post
title: Rational Bloom Filters 
---
This blog post is to introduce my masters thesis, "Rational Bloom Filters". I will be using this blog to write about my thesis and to discuss
interesting technical challenges I encounter along the way. If you are a human that happens to be reading this, hi👋. Anyways, what is my thesis about?
Essentially the idea is to use some novel ideas about Bloom Filters for lossless compression. These novel ideas are originally not my own and because they are not yet published
I will not discuss them in detail. However they revolve around reducing the integrality assumption about the number of hash functions needed for a Bloom Filter. This allows
for fine tuning of the false positive rate that wasn't previously possible before. Without spoiling unpublished work, we are not so much interested in reducing the false positive rate, rather
reducing the total size of the bloom filter. This is because we wish to use these novel ideas to use the Bloom Filter to compress arbitrary input in a lossless fashion. In particular I am interested in 
furthering the (currently)unpublished work by investigating techniques to use the bloom filter for lossless video compression. I plan to make a number blog posts that will serve as a useful guide for those new to video 
compression. However realistically nobody will read these posts so its more of an excuse for me to talk to myself about technical challenges...stay tuned for the next post

