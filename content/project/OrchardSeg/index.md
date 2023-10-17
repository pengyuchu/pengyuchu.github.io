---
title: Orchard Segmentation
summary: Panoptic segmentation in the orchard for fruit harvesting robots.
tags:
  - Research
date: '2023-09-19T00:00:00Z'
# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: ''
  focal_point: ''
  placement: 2
  preview_only: true

# links:
#   - icon: twitter
#     icon_pack: fab
#     name: Follow
#     url: https://twitter.com/georgecushen
# url_code: ''
# url_pdf: ''
# url_slides: ''
# url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
# slides: example
---

{{< video autoplay="false" loop="false" src="demo.mp4" controls='yes' >}}


One of the key challenges faced by harvesting robots is the ability to recognize their surrounding environments. The real-world environment of a tree-grown orchard is inherently complex, making it difficult for harvesting robots to navigate and perform tasks while avoiding obstacles such as branches and foliage, while also accurately identifying and interacting with the fruit.



In response to this challenge, we developed the panoptic-DeepLab architecture tailored specifically for orchard environments. This architecture enables us to not only identify the main obstacles but also pinpoint the target, which, in our case, is apples for our harvesting robot. Our system segments each scene (see **Fig. 1**) into five distinct categories: apple, branch, foliage, sky, and ground. This dataset encompasses a wide range of orchard scenes, fruit morphologies, and various environmental conditions, thereby providing a comprehensive representation of real-world fruit detection scenarios.

<center>{{< figure src="fig1.png" title="Figure 1. Orchard segmentation results. " >}}</center>

Given that branches pose the most significant obstacle, we have further developed skeleton-lead CNNs. This network works to skeletonize the branches (see **Fig. 2**), effectively transforming them into graph structures, resulting in improved branch segmentation accuracy. As a by-product, the branch graphs can also be leveraged to efficiently construct a 3D representation (see **Fig. 3**) of the scene using corresponding depth images. This wealth of data serves as crucial input for robotics planning and decision-making processes.

<center>{{< figure src="fig2.png" title="Figure 2. Branch graphs outputed by skeleton-lead CNNs. " >}}</center>

<center>{{< figure src="fig3.jpg" title="Figure 3. 3D representation of branches and apples." >}}</center>