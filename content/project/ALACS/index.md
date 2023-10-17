---
title: 'ALACS: Apple Localization'
summary: An apple 3D Localization technique using laser-camera triangular principle.
tags:
  - Robotics
  - Research
date: '2023-02-07T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: ''
  focal_point: ''
  placement: 2
  preview_only: true

links:
  # - icon: twitter
  #   icon_pack: fab
  #   name: Follow
  #   url: https://twitter.com/georgecushen

# url_pdf: 'https://elibrary.asabe.org/'
# url_code: 'https://github.com/wowchemy/wowchemy-hugo-themes'
# url_video: ''
---
{{< video autoplay="false" loop="false" src="demo.mp4" controls='yes' >}}

While industry depth cameras (like RealSense RGB-D camera) are compact and capable of providing rich environmental information, its depth measurements are susceptible to variations in lighting conditions and exhibit instability when apples are partially obscured by branches or foliage. These limitations have been identified as the primary culprits behind the inaccuracies in apple localization, a problem that was evident in our previous field tests. In light of these issues, we have developed an Active Laser-Camera Scanning Scheme (ALACS), illustrated in **Fig. 1**, with the aim of improving the precision of apple localization.

<center>{{< figure src="fig1.jpg" title="Figure 1. ALACS device." >}}</center>

ALACS employs the [triangulation technique](https://www.movimed.com/knowledgebase/what-is-laser-triangulation/) (see **Fig. 2**) to determine 3D positions. We have opted for a laser line as our 2D pattern because of its superior stability and robustness. Thanks to the laser scanning mechanism, we can obtain multiple pattern candidates (see **Fig. 3**) along with their respective positions, thereby mitigating the risk of inaccuracies, such as occlusions.

<center>{{< figure src="fig2.jpg" title="Figure 2. Laser Triangulation." >}}</center>

<center>{{< figure src="fig3.png" title="Figure 3. 2D patterns from  laser scanning." >}}</center>
