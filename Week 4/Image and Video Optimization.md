# Image and Video Optimization

## What is image optimization?

Image optimization is about reducing the file size of your images as much as possible, without sacrificing quality, so your page load times remain low. It's also about image SEO—that is, getting your banner and product images to rank highly on Google and other image search engines.

## How can you optimize images and speed up your site?

- Reduce the number of images. Remove them.
- Concatenate images into single files (i.e., image sprites)
- Load critical images first
- Prioritize above-the-fold content
- Compress and reduce image data as much as possible without compromising acceptable quality.

## Convert to the right format

JPEG is the default format in the web. PNG may work better with graphic designs featuring solid colors, but in these cases it may yield lower weight with better quality.

You may consider offering WEBP for Chrome, Edge, Firefox and Android users, keeping JPEG as fallback for Safari and iOS. It may save 10-30% of image weight with very similar quality, perhaps some more blur and less ringing.

## Get rid of metadata

From shooting to editing, images accumulate metadata, like exif data. While they may be useful for editing and management purposes, they have no impact on how images show in our web. Their weight can easily get 20 KB or more per image.

We should get rid of metadata before publishing on the web. We only have to make sure that images are coded with the proper orientation and with a sRGB profile, adhering to good color management practices.

## Video Omptimization

As we learned in the previous section, media, namely images and video, account for over 70% of the bytes downloaded for the average website.

## Why optimize your multimedia?

For the average website, 25% of bandwidth comes from video. Optimizing video has the potential for very large bandwidth savings that translate into better website performance.

## Optimizing video delivery

The sections below describe the following optimization techniques:

- compress all video
- optimize source order
- set autoplay
- remove audio from muted video
- optimize video preload
- consider streaming

## Compress all videos

Most video compression work compares adjacent frames within a video, with the intent of removing detail that is identical in both frames. Compress the video and export to multiple video formats, including WebM, MPEG-4/H.264, and Ogg/Theora.

Your video editing software probably has a feature to reduce file size. If not, there are online tools, such as FFmpeg (discussed in section below), that encode, decode, convert, and perform other optimization functions.

## Optimize source order

Order video source from smallest to largest. For example, given video compressions in three different formats at 10MB, 12MB, and 13MB, declare the smallest first and the largest last:

```HTML

<video width="400" height="300" controls="controls">
  <!-- WebM: 10 MB -->
  <source src="video.webm" type="video/webm" />
  <!-- MPEG-4/H.264: 12 MB -->
  <source src="video.mp4" type="video/mp4" />
  <!-- Ogg/Theora: 13 MB -->
  <source src="video.ogv" type="video/ogv" />
</video>

```

The browser downloads the first format it understands. The goal is to offer smaller versions ahead of larger versions. With the smallest version, make sure that the most compressed video still looks good. There are some compression algorithms that can make video look (bad) like an animated GIF. While a 128 Kb video may seem like it could provide a better user experience than a 10 MB download, a grainy GIF-like video may reflect poorly on the brand or project.