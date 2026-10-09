---
title: "008 -  The Execution Timeout (504 Gateway Timeout)"
slug: "008-the-execution-timeout-504-gateway-timeout"
date: "2026-07-23T16:09:38"
categories: ["Uncategorized"]
---
[![](http://yonilexxs-error-encyclopedia.local/wp-content/uploads/2026/07/Ekran-goruntusu-2026-09-05-185353-1024x576.png)](http://yonilexxs-error-encyclopedia.local/008-the-execution-timeout-504-gateway-timeout/ekran-goruntusu-2026-09-05-185353/)

**What is this error:** This is not a beheading, so do not worry. So, your browser screen completely locks up, loads, loads, and loads, and then you get jumpscared by **"504 Gateway Timeout**" or ''**Maximum Execution Time Exceeded**'' and the website does not open because the server already gave up.

**''I need more quotes.''**

So**, the source of this is usually:** The website asked the server to do some heavy lifting **(like generating a massive report or processing huge files). The server tried, but it took too long. Because the server has a built-in strict timer, it got tired, cut the connection, and fainted.** Think of it like a waiter is walking to your table with your food, but the food is too heavy, so he faints.(Poor guy)

**''I definitely need more quotes.''**

**How to wake up the server:**

**Acess the root folder via `SSH` or `FTP` and find our favorite file: Yes, `wp-config.php`**

To give the server **more time**, simply **elaborate further** **with this line** (**Right above** the **stop editing line**)

`**set_time_limit(300);**`  
(Server now has 300 seconds. Server happy, yay!)

Note: Hmmm, this one was very short!

[1999 - 2020 R.I.P Flash Games](https://www.youtube.com/watch?v=GQltMXdN7ZM&list=RDGQltMXdN7ZM&start_radio=1)
