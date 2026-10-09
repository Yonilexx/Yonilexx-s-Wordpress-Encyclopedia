---
title: "006 - Too Many Redirects"
slug: "006-too-many-redirects"
date: "2026-07-24T14:40:30"
categories: ["Uncategorized"]
---
[![](http://yonilexxs-error-encyclopedia.local/wp-content/uploads/2026/07/Ekran-goruntusu-2026-09-04-163107-1024x576.png)](http://yonilexxs-error-encyclopedia.local/006-too-many-redirects/ekran-goruntusu-2026-09-04-163107/)

**What this error is**: The browser screen turns white or grey and displays a cold error message that reads: _"**This page isn’t working**, **site redirected you too many times**"_ or _"_**_ERR\_TOO\_MANY\_REDIRECTS_**_"_. The site is trapped in an infinite loop and completely refuses to load. (Stubborn)

this error **might seem very complex** and **brain\-demanding**, but no, **it's not a zombie** that eats brains!

**So**, **the source of this is** **usually**:

The ''**WordPress Address(URL**)'' and the ''**Site Address** (**URL**)'' **settings** are **having beef with each other.** The **website wants to go to point A**, **but the server wants it at point B**. **Then point B takes our poor website to point A**. **If an SSL** (**HTTPS**) **plugin is also fighting with the server's `.htaccess` file**, the website enters a loop. (Like how a hamster spins a wheel.)

**''I don't know how else you could ask for the fix, so here is the fix''**

*   **Access the Heart**: Connect to the server via **SSH** or **FTP** and **navigate to the root folder** (`**public_html**` or `**www**`). Open the **`wp-config.php file`**(Yes, again. I guess IT really consists of using the same methods even in different situations, but that is the charm of it!)
*   **Break the hamster wheel**(**No hamsters were harmed during the preparation of this blog. I don't even own a hamster!**): Scroll down and find the line that reads ''**`/* That's all, stop editing! Happy publishing. */`'**'. Right **ABOVE**(**important**), paste these two magic lines to lock the URLs:
*   `**define('WP_HOME','https://yourdomain.com');   define('WP_SITEURL','https://yourdomain.com');**`

(**Please remember to change `yourdomain.com` to the customer's actual live website URL**. **I know some day someone will copy-paste this! (It's you!)**  
  
[We all lift together.](https://www.youtube.com/watch?v=mPTCq3LiZSE&list=RDmPTCq3LiZSE&start_radio=1)
