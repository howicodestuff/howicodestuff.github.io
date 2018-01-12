---
layout: post
title: "Vim: Basic Usage"
date: 2018-1-17 13:50:00
categories: Development Tools
excerpt: "Vim (Vi IMproved) is a renewed edition of Vi, which provides functionality unmatched by any other text editor. Let's check out how it works!"
---


1. [Introduction](#intro)
2. [Why would I use Vim?](#why)
3. [Opening a File for Editing](#open)
4. [Insert Mode](#insert)
5. [Searching](#search)
6. [Save and Exit](#exit)
7. [Learning More On Your Own](#vimtutor)
8. [Synopsis](#synopsis)

<a name="intro"></a>
### Introduction

Open a terminal in any \*nix system and type `vi`. Chances are you'll be welcomed by this lightweight but really powerful text editor.

Vim (Vi IMproved) is a renewed edition of Vi, which provides functionality unmatched by any other text editor - unless, of course, it has a Vim plugin!

<a name="why"></a>
### Why would I use Vim?

There is no generic answer to this question. After all, you'll be fine never learing how to use Vim at all - you can make do with other tools. For some people however, it's their most important tool for being as productive as they can be. Some of the reasons to get into Vim are presented below:

* **Lightweight**
	  You will be able to use it with any system, file or project, in contrast with resource-heavy text editors like Visual Studio or Atom, and IDEs like Eclipse or Intellij products, which might choke under the pressure of huge files or projects.

* **It's Everywhere**
	  If you ever get into working with servers, you'll quickly find out that Vi or Vim are almost always already in the list of installed software.

* **Poductive**
	Vim has the philosophy of a language - it's commands have verbs, nouns and adjectives which can be chained together in infinite combinations. For example, the command `d3w` (delete 3 words) is comprised of 3 different parts. The `ci"` command(change inside ") will delete the text inside the " " your cursor is in and put you in insert mode so you can write in there. Vim also provides a very useful tree representation for the redo (`CTRL+R`) and undo (`u` and others)  commands, a multitude of registers for copy (`y` - yank) and cut commands - you can paste from many different clipboards, which arms you with a lot of functionality - and it can execute bash commands and show you their output, which you can optionally insert into your file.

* **Ergonomic**
	  Vim's philosophy distances you from use of the mouse, and encourages movement by using the keyboard, making it faster and healthier for the wrists, eyes and tendons.

* **Fun**
	  Vim is just really, really interesting, and everything new you get to learn about it gives you a feeling of satisfaction, in the neverending process of discovering new ways of doing old things faster and better.

* **FOSS**
	  Vim's licence is GPL-compatible, and anyone can view and contribute to it's source code. This means that thanks to it's enormous number of users, it never stops evolving.

* **Configurable**
	  You can very easily configure Vim to exactly your liking, more so than any other editor available. It's very common for each user to have their own config files and copy them to each machine they use. Many of us post our configs online, usually called "dotfiles".

In this article we won't get into great detail on Vim's abilities, but we will explore it's basic usage for editing a file. Students, web developers, Linux, MacOS and other \*Nix users often tend to need it in order to change a remote file or edit a file as administrator.

<a name="open"></a>
### Opening a File for Editing

Launch a terminal, and either locally or after connecting remotely to an SSH session, open some file, for example `file.c`:

```console
vim file.c
```

If the file does not exist, it is created. If it does, it is opened for editing. Try to enter "22222222"

```vim
222222222
```

You can see that nothing is happening. This is because we are in **comand mode**. To change the file, we can press `i`. This will put us in **insert mode**.

<a name="insert"></a>
### Insert Mode

We can make changes to the file. For now, navigate with the arrow keys.
After we make any changes we want, we can exit from insert mode by pressing the <button>ESC</button> key.

<a name="search"></a>
### Searching

To do a search for something, from the command mode, we press `/` and enter the string or regular expression we want to search for.

```vim
/search-phrase
```

If there are any results, we can press `n` to go to the next result and `N` to go to the previous one.

Click on the image to see it in action.

<a name="exit"></a>
### Save and Exit

To save the changes we made to the file, we have to go to command mode, and press `:`. This will bring us over to **last line mode**

```vim
:
```

Here we can execute bash commands, for example `ls`, by putting a `!` in front of them like so:

```vim
:!ls
```

...but we'll go into that in a future article. For now, let's write our changes:

```vim
:w
```

To exit Vim, we can give the `q` command in last line mode:

```vim
:q
```

Remember how, in the beginning of the article, I talked about chaining commands together? Well, we can save and exit by combining the previous two commands:

```vim
:wq
```

If we want to exit without saving, Vim is going to whine. We can force quit by entering:

```vim
:q!
```

<a name="vimtutor"></a>
### Learning More On Your Own

Vim comes with an exceptional tool for learning it how to use it, called "Vim Tutor". It explores navigation by using the home row keys hjkl (which is the best way to navigate in Vim), as well as finding your way around words, sentences, parentheses and many more, as well as going into replace mode, which I haven't covered in this article. To try it out, type in your terminal:

```console
vimtutor
```

<a name="synopsis"></a>
### Synopsis

Vim is a really useful tool that provides us with unmatched productivity, ergonomy and above all, is fun to use and configurable to any person's needs.

In this article we went through some of it's basic usage, such as changing text, searching and saving. In the future I will add a series of articles where we can explore Vim's abilities in depth.

\**I wrote the Greek version of this article for the IEEE University of Ioannina Student Branch. You can check it out [here](http://ieeesb.uoi.gr/?p=2237)*