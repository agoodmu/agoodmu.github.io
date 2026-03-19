---
title: "Digital Forensic Imaging" # Title of the blog post.
date: 2025-07-22T10:26:17+12:00 # Date of post creation.
description: "How to image storage device for forensic purpose" # Description used for search engine.
featured: true # Sets if post is a featured post, making appear on the home page side bar.
draft: true # Sets whether to render this page. Draft of true will not be rendered.
toc: false # Controls if a table of contents should be generated for first-level links automatically.
# menu: main
usePageBundles: false # Set to true to group assets like images in the same folder as this post.
featureImage: "/images/path/file.jpg" # Sets featured image on blog post.
featureImageAlt: 'Description of image' # Alternative text for featured image.
featureImageCap: 'This is the featured image.' # Caption (optional).
thumbnail: "/images/path/thumbnail.png" # Sets thumbnail image appearing inside card on homepage.
shareImage: "/images/path/share.png" # Designate a separate image for social media sharing.
codeMaxLines: 10 # Override global value for how many lines within a code block before auto-collapsing.
codeLineNumbers: false # Override global value for showing of line numbers within code block.
figurePositionShow: true # Override global value for showing the figure label.
categories:
  - Technology
  - Security
  - Forensics
tags:
  - Security
series:
  - Digital Forensics
# comment: false # Disable comment if false.
---

** dd **
dd if=/dev/sda of=forensic.dd conv=sync,noerror
md5sum forensic.dd
sha256sum foresic.dd
losetup --partscan /dev/loop0 /data/forensic.dd
mkdir /mnt/local
mount /dev/loop0 /mnt/local
** dcfldd **
dcfldd if=/dev/sda of=forensic.dd conv=sync,noerror hash=md5 hashlog=forensic_hash.txt
** dc3dd **
dc3dd if=/dev/sda of=forensic.dd hash=md5 log=forensic_hash.txt


foremost -i /dev/loop0 -o output


losetup --find --read-only --partscan --show case9_2024.dd
The dd im
