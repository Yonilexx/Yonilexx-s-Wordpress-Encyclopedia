---
title: "012 - Disappearing Act of Items In Cart"
slug: "012-disappearing-act-of-items-in-cart"
date: "2026-07-12T17:29:09"
categories: ["Uncategorized"]
---
You add items you want in the cart and after a few seconds the cart is empty and the site says ''Your cart is empty'' like some kind of bad antivirus.(You know, they always point you to wrong stuff or don't point at all.)

_''**The quote writer me quit his job so uh, who wants to work as my quote guy?**''_

This is usually because:  
  
**Caching**: Speed plugins or server-side cache systems bullying your dynamic cart pages.

**Session and Cookie Mismatch**: The browser losing the **wp\_woocommerce\_session\_** cookie like you've lost erasers at school.

**Fauly Permalinks or Endpoints**: A broke or a permalink structure you forgot to flush causing WooCommerce AJAX endpoints to hit 404 errors, breaking cart fragment updates and assasinating the active session state during the redirection to checkout.

''**_Who can think 100+ different and cool ways of asking why/the fix anyway?_**''

*   **Checking Caching Plugin Settings**: Go to your caching plugin settings (WP Rocket, LiteSpeed, etc.) and ensure that the **Cart**, **Checkout** and **My Account** pages are explicitly **EXCLUDED FROM CACHING**. (or no fix for you.)
*   **AJAX Endpoints**: Make sure WooCommerce AJAX endpoints(**wc ajax=get\_refreshed\_fragments**) are bypassed by your cache rules. This means in human language you need to add **?wc-ajax=\*** to your caching plugin's URL exclusion list under its Advanced Settings tab, configure your Nginx/Apache server configuration file to skip cache **woocommerce\_items\_in\_cart** cookie is there or use a custom endpoint-skipping filter right into your theme's **functions.php** file so the server finally stops caching dynamic cart fragments like they're static.  
    
*   **Session Configuration**: Check your server's session configuration. To do this you can use WP-CLI and type **wp user meta get session\_tokens** or do this from your database manager (phpMyAdmin, Adminer, DbGate etc.) with this code:

[Youtube was in it's prime with this man.](https://youtu.be/Yy-NyPTRYU8?si=xee93eLhhEOJSfcX)
