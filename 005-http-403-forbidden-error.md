---
title: "005 - HTTP 403 Forbidden Error"
slug: "005-http-403-forbidden-error"
date: "2026-07-25T18:56:29"
categories: ["Uncategorized"]
---
[![](http://yonilexxs-error-encyclopedia.local/wp-content/uploads/2026/07/Ekran-goruntusu-2026-08-31-175815-1024x576.png)](http://yonilexxs-error-encyclopedia.local/wp-content/uploads/2026/07/Ekran-goruntusu-2026-08-31-175815.png)

*   Website is a locked fortress and is now just showing ''**HTTP 403 Forbidden**'' >:(
*   The server decided to be a bodyguard and threw an "**Access Denied**" sign in our faces to make us angry. (Always)

''_I know,_ _but why is this happening_?''

1.  **Corrupted .htaccess rules**: **A security plugin** got too aggressive and **locked the entire directory** because why not?
2.  **Wrong File Permissions**: **The server folders** are **set to very, very wrong permissions**. So, **the system is blinding itself**.
3.  **Faulty Security Plugins**: **Wordfence** or **iThemes** got **confused,** pressed all the keys at once, and **blacklisted everyone**.

''_I know, just tell me the fix_!''

How to **bypass Mr.security guard**?(It's like lockpicking, but you lost the keys to your own house.)

*   **Reset the .htaccess:** **Log into your hosting via File Manager** and **go to your root folder**, **find the '.htaccess' file**, **rename it** to **'.htaccess\_old'** (just like we did to plugins not long ago!), and refresh the site. **If it loads**, your **.htaccess file was being crazy**. Go to **Settings -> Permalinks** and **hit that save button** to generate a new (mentally) **stable .htaccess file!** ...Why are you still here? ...Oh.
*   **Fix the Permissions Numbers**: If **.htaccess** was a good boy, **your folder permissions must be messed up**. **Go to File Manager**, right-click on **public\_html**, and **make sure** **Folders are set to 755 and Files are set to 644**. **Do not(important) give wrong numbers,** or your server will get a processor **(**heart of computers**)** attack. **Treat your devices well,** please!
*   **Disable the Plugins**: NO, NOT THIS AGAIN, NOOOO! Ugh, anyway, go to 001 and apply the ''**Isolate the Plugins**"

The **Ultimate SSH Secret**(Not a secret anymore): If you have **SSH Access** and want to **fix all file permissions instantly** without clicking 100 times, **run these two lines in your root folder**:

**  
`find . -type d -exec chmod 755 {} \;`  
`find . -type f -exec chmod 644 {} \;`**

[Johnny wasn't the one who bombed Arasaka HQ btw.](https://www.youtube.com/watch?v=Igq3d6XA75Y&list=RDIgq3d6XA75Y&start_radio=1)
