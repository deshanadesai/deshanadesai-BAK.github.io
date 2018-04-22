---
layout: post
title: Find Salient colours in a region inside an Image.
category: posts
---

Our goal is to find the main colors in a region of an image. 

First, we need a list of all the RGB values of the pixels in the region we are considering.
Next, we are going to use clustering to find different groups of colours. 
We are then going to filter out the groups that are not dominant enough for us.
We are going to follow up by evaluating how well the clustering method performed.
And finally, find the corresponding human colour for the RGB values.
