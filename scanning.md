---
layout: page
title: Scanning
permalink: /scanning/
---

The following page contains a brief overview of **how to take good images** of the wall/boulders so that Climbuddy can reconstruct them.
It is generally applicable for any type of 3D reconstruction, but all of the examples will be specific to Climbuddy.

## Requirements

To effectively capture images for 3D scanning, you'll need a decent **mobile phone** or camera capable of producing high-resolution images.
It's recommended that the images have dimensions of at least **2000×1000 pixels** to ensure detail in the final reconstruction.

It's also strongly advised to **use raw images**, since it bypasses kind of retouch/enhance funtionality, which is prominent in most recent mobile devices and reduces the quality of the 3D reconstruction.
This can generally be done in the following ways:
- for *Android*, [set format to RAW](https://www.androidpolice.com/android-capture-edit-raw-photos-guide/)
- for *iPhone*, [enable ProRAW](https://support.apple.com/en-us/HT211965)

## Scanning

A good approach for taking images is to start on one side of the wall and do the following:
1. turning left-to-right (or right-to-left), **take overlapping images** of the wall
2. **move one step** along the wall
3. **repeat** until the entire wall is captured

This approach makes sure that you cover the entire wall and that all parts have a good number of angles they are captured from, making the reconstructed geometry detailed and correct.

TODO: sample video here (from the POV of the mobile phone)

There are two things you must keep in mind when taking the images: **overlap** and **blur**.

### Ovelap

Overlap in images is essential for reconstruction as it enables accurate reconstruction and camera localization.
It's advisable that when turning around, the subsequent images have **at least a 30% overlap**.

<figure class="center standout">
  <img src="/assets/scanning/good-overlap.webp" alt="TODO">
  <figcaption>An example of <strong>sufficient overlap</strong> – at least a third of the image is overlapping.</figcaption>
</figure>

<figure class="center standout">
  <img src="/assets/scanning/bad-overlap.webp" alt="TODO">
  <figcaption>An example of <strong>insufficient overlap</strong> – there is not enough overlap between the two image.</figcaption>
</figure>

While it is not necessary to follow this rule for _all subsequent images_, it is generally good to keep in mind as you're taking the images, since this what most of the underlying algorithms are using when reconstructing the models.

### Blur

Having clear images is another important part crucial for accurate 3D reconstruction.
Clear images provide distinct features that algorithms use to calculate depth and camera positions, which cannot be inferred from blurry images.

<figure class="center standout">
  <img src="/assets/scanning/good-bad-quality.webp" alt="TODO">
  <figcaption>An example of <strong>good</strong> (left) and <strong>bad</strong> (right) image quality – blurry images cannot be used.</figcaption>
</figure>

Having a _few blurry images is okay_ since the reconstruction software can automatically detect this (i.e. it is not necessary to go through the images and manually filter them out), but it should be an exception and not the rule.

If you're having issues with taking clear images, you can try to **increase the shutter speed** (as a tradeoff to increasing ISO and thus making the images a little more noisy), although most mobile phones should do this automatically and without too much trouble.

## Summary

To summarize, a good dataset for image reconstruction should

- **cover the entire object** from **multiple angles**,
- have **good overlaps** between images and
- limit **blur** as much as possible

If there are any issues you run into, or you think that something in this article is incorrect, feel free to shoot us an email at [contact@climbuddy.com](mailto:contact@climbuddy.com).

Happy scanning!

{: .right}
_Team Climbuddy_
