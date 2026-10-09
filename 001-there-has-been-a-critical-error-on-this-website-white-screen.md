---
title: "001 - There Has Been a Critical Error on This Website (White Screen)"
slug: "001-there-has-been-a-critical-error-on-this-website-white-screen"
date: "2026-07-27T00:37:42"
categories: ["Uncategorized"]
---
[![](http://yonilexxs-error-encyclopedia.local/wp-content/uploads/2026/07/Ekran-goruntusu-2026-08-24-175533-1024x576.png)](http://yonilexxs-error-encyclopedia.local/wp-content/uploads/2026/07/Ekran-goruntusu-2026-08-24-175533.png)

''What is the reason for this error?''

This can have a few reasons, but don't worry; this blog or I will help you fix it.  

1.  Plugin or Theme Conflict(Betrayal)
2.  Your site is trying to use **a lot of resources**. (**Exhausted Memory Limit**)
3.  **Syntax Error** (Tired Developer): Someone was editing code directly and **forgot a single semicolon or closed a bracket very wrongly****.**
4.  **Broken Core Files**: **A core** **WordPress update got interrupted halfway through** because of a very **inconvenient connection time-out** (I hate disconnections too)

''_**But how am i gonna fix this mess**_?''

**I am conveniently placing the fixes I know**:

1.  **Isolate the Plugins**: Log into your hosting via **File Manager**, go to **wp-content/plugins**, and **rename the most recent plugin** to **plugin-name-old.** If the site loads, you're welcome. If not, proceed to the next step.
2.  **Switch the Theme**: So, the **plugins were innocent** this once. So, our next target is the **theme**. Go to **wp-content/themes** and **do the same thing you did to plugins.** I hope it worked this time! It didn't work? Aw man.
3.  **Boost the Memory**: Open your **wp-config.php** file and add this spell line right before the ''**Happy Publishing**'' text to give your server more brain (**More brain=Smarter**) `define( 'WP_MEMORY_LIMIT', '256M' );`
4.  **Syntax Error**: Delete that semicolon or fix the bracket. Easy and Quick!

OR...

**The Forbidden Art of WP-CLI.**

If you prefer the very secret technique, the **Command Line**, simply **SSH(Secure Shell)** into your server, navigate to your **root folder**, and run:

*   `tail -n 50 wp-content/debug.log (WordPress logs)`
*   `**tail -n 50 /var/log/nginx/error.log** (Nginx logs`)
*   `tail -n 50 /var/log/apache2/error.log **(Apache logs)**`

**After using these codes**, you should **check the logs** and **see which plugin is fighting your site's order**. Then **disable that plugin**.

**Note**: ''Fatal error'' page is what engineers would like to see; ''Critical Error'' page is what the customer should see, so the business's reputation doesn't go down.

[Lines are for aesthetic and music links!](https://www.youtube.com/watch?v=TGASYGTTC34&list=RDTGASYGTTC34&start_radio=1)
