---
title: "007 - The Lost Key (WordPress Password Reset via PhpMyAdmin)"
slug: "007-the-lost-key-wordpress-password-reset-via-phpmyadmin"
date: "2026-07-23T23:09:25"
categories: ["Uncategorized"]
---
So, you **completely forgot your WordPress admin password** **(happens)**, and the **usual** ''**Lost your password****?'' recovery email is stubborn enough not to send or arrive at you**. So you're totally locked out.  
  
**''Please don't expect me to find different and cool quotes for each ''why'' section''**

This is usually **because of a server-side email configuration issue** (For example, **missing SMTP settings**). Since **the site cannot send emails, you** (Unfortunately) **cannot reset your password the traditional way**. As if you **forgot your keys** but **can't call a locksmith,** so you have to... **change the lock** and make it **fit whatever key you have in mind**!

How to change the lock to fit the key you have :

1.  **Enter the Database Engine**: Log into the **cPanel**/**Plesk** and find the tool named `**phpMyAdmin**`
2.  **Find the Users Section**: On the left sidebar, click on the site's databases, then look for the section named **wp\_users** (**Very important note**: This might be something else like **wp\_custom\_users**, look for the **\_users** part)
3.  **Edit the Admin User**: Find the admin username, and click the ''**Edit**'' next to it.
4.  **The Cool MD5 Trick**: Look for the row named user\_pass. Change the ''Function'' (By the way, I never understood functions at school for some reason) dropdown to **MD5** (**This is ultra crucial to encrypt the password). Then, in the ''Value'' box, type their brand-new, safe password**.
5.  **Save and Enter**: **Scroll down**, click ''**Go**'' to leave. The lock's changed now.
6.  **Be Careful not to forget your password again**!

[Zombies, guns, carpentry and metal music.](https://www.youtube.com/watch?v=5fmXjVuyVKo&list=RD5fmXjVuyVKo&start_radio=1)
