---
layout: post
title:  "Late Additional Experiments for Attention-based LVSR"
date:   2016-03-27 21:08:37
categories: jekyll update
---

A few months ago I carried out a few additional experiments with the system
described in our paper [End-to-end Attention-Based Large Vocabulary Speech
Recongition](http://arxiv.org/pdf/1508.04395v2.pdf). Unfortuntely, I lost
access to the training logs and models since then (never leave a backpack with
important stuff in it unattended in a bar...). However, I still remember the
important findings, which I am glad to share here with you:

1. The pretraining stage with expanding window turned out to be *not necessary*
   for the system with a good deal of subsampling in the encoder, such as the
   one for which we reported the results.

2. Simply changing the batch size to 1 from 10 brought 15% improvement to our
   CER without the language model. Unforunately, I did not have time to evalute
   the model with the language model. Seems like a small batch size can be a very strong    but very expensive regularizer, training took 3 weeks instead of 1.
