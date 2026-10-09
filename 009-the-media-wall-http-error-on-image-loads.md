---
title: "009 - The Media Wall (HTTP Error on Image Loads)"
slug: "009-the-media-wall-http-error-on-image-loads"
date: "2026-07-22T18:37:25"
categories: ["Uncategorized"]
---
So, **what exactly is this error**: You open your **WordPress Media Library**, select a very normal **JPG** or **PNG** image, and **smash the upload button**. The **loading bar fills,** but right **at the end it turns red and displays a stubborn message**: **_"HTTP Error"_** and nothing else. **The site refuses to just accept your image**(Wish it did)

''_**Imagine there is a quote about jumping to the fix instead here**_''

Well, **I'll cut this short(Because I don't want to steal your time like this parenthesis.)**: You can't upload image because your **PHP Memory Limit is too low**, so it **chokes, coughs and spits out the image.**

**How to increase memory limit:**

Open **root folder** via **SSH** or **FTP** and open the very specific**, definitely not-so-common** file **`wp-config.php`**(As I said before, **it is the charm of IT**), and **paste this code right above the stop editing line:**  
`**define( 'WP_MEMORY_LIMIT', '256M' );**`

Server happy, server got more memory, server now remembers more things!(Protect servers at all costs)

[You're the Most Wanted Human Wrangler now. Need for Talent!](https://www.youtube.com/watch?v=auywWyLVkng&list=RDauywWyLVkng&start_radio=1)
