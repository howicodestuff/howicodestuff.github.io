---
layout: post
title:  "Coding On The Go"
date:   2017-12-24 20:00:00
categories: General Development Tools
---

Coding on the go - the title is pretty self-explanatory, but my motives for writing this article not as much. Let's dive in to why before going in to how.

### Why would I code on the go?

Personally, I have to. My family owns a small hotel in the Greek mountains, and I have to be there for most holidays and some weekends, which means I have to do my dev work and studying there. I also have a lot of free time between classes in university and I prefer to use them instead of having coffee etc.

Your reasons might be different. You might like travelling, you might have family to visit in another area code or state or even country. Your work itself might involve giving presentations or meeting with clients in different places. This article is not about that. It is about efficiently managing your limited laptop resources and screen real estate.

### What is the ideal screen size?

Well, there's no one-size-fits-all, or else there wouldn't be any other choice in laptop screens. This largely depends on how portable you want your setup to be, what kind of work you do, and how willing you are to adjust your normal way of doing things.

At home, I always have half my screen having a browser open so I can see the application I'm working on, and half my screen having a sophisticated editor or IDE - lately that's been Visual Studio Code.

However, that's just not practical on my old Thinkpad's 12.1" screen.

What is practical about it is it's portability; I can put it in my backpack and take it anywhere, in contrast with a bigger and heavier laptop. If you primarily work from your hotel room, you might be better off having a bigger laptop, preferably with a nice full HD IPS screen. For everyday carry, I strongly suggest going as small as you can in screen size.

### How can I work with such limited screen space?

Workspaces and terminals. I have set up six workspaces on this machine, and every one of them holds something different. I have configured my shortcuts to make switching between them super easy (Super-Z, Super-X, Super-C, Super-V for the four main workspaces; moving around with CTRL-ALT-arrow to use the other ones)

My first workspace holds the browser. I work in web application development so a browser has to be open 24/7 - and that's where it lives. 

The second workspace has my text editor. For work, I use Visual Studio Code. For pretty much everything else, I use Vim.

The Git client lives on the third workspace. I use GitKraken. It has it's own workspace because I spend a lot of time looking at diffs.

My fourth workspace has a full screen Terminator session. Terminator is a terminal emulator which supports having multiple terminal windows and easily creating/deleting/moving between them. Here, I can always check out my system resources, do all my npm installs, quick edit a file, move between directories etc.

The fifth and sixth workspaces are situational; If I need to manage a database, that's where I'll have MySQL Workbench. If I need to post a bunch of mock data to an API, I'll open Postman there. I'll also open chat clients here if I have to be in constant communication with someone.

Moving windows around workspaces is bound to CTRL-Shift-(Z-V for main workspaces, or arrow keys for the 2 situational ones).

On my desktop computer I will still use the split view because it is more convenient. However, the difference is really very small after you get used to moving around workspaces like that.

### Conclusion

You can make a small laptop work really well for you if you set it up right. In my opinion, it's worth it to invest some time in learning how to work with a smaller screen. Even at home, I find myself opening the laptop lid and doing quick checks or edits on files there instead of my big powerful desktop, and the reason is simple; sometimes, it's just more convenient to just sit by the firplace or have the laptop sit next to me while I'm cooking, than going to my desk and turning on the desktop computer.

Thank you for reading. I hope to see you again on the next one!

PS: Pro tip - if you have the space in your luggage, carry with you an HDMI and maybe even a VGA cable. Most hotels or places you'll visit will have a TV you can turn into a second monitor. 
