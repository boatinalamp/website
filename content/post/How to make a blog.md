---
title: "My First Blog Post"
date: 2022-11-12T12:51:42+05:30
draft: false
---
# My First Blog Post
While painfully configuring this server.I realised I was missing out on something. CONTENT, I was worried that after all my hard work, I wouldn't have anything to write about. So I set out, desperate for something, anything to write about.
I found nothing, so I'll just write about how I created this blog.
# Installing Hugo
To install hugo, i used scoop package manager
```scoop install hugo-extended```
# Creating the server
To create the servers base files, i just used hugo itself
```
hugo new site MyBlog
cd MyBlog
```
# Installing themes
In the root directory of the server, I ran
```
cd themes
wget https://github.com/jbub/ghostwriter/archive/master.zip
```
I then unzipped (unpacked) the master.zip folder.
# Configuring Server
Inside the root directory of the server, I created a `config.toml` file, inside it I put
```
baseurl = "/"
title = "NAMEOFBLOG"
theme = "NAMEOFEXTRACTEDFOLDERINTHEMESFOLDER"

[Params]
    mainSections = ["post"]
    intro = true
    headline = "WHATYOUWANTTODISPLAYATTHETOP"
    description = "DESCRIPTION"
    github = "URGITHUB OPTIONAL"
    twitter = "URTWITTER DELETE LINE IF U DONT WANT"
    email = "UREMAIL DELETE LINE IF U DONT WANT"
    opengraph = true
    shareTwitter = true # set to false if not sharing twitter
    dateFormat = "Mon, Jan 2, 2006" # leave as is

[Permalinks]
    post = "/:filename/"
```
# Creating a post
back in the root directory of the server, type
```

	hugo new content/post/NAMEOFPOST.md```
replacing NAMEOFPOST with the name of your post
than open the `SERVERDIRECTORY/content/post/NAMEOFPOST.md file with your editor of choice, mine is notepad, replace `draft = true` with `draft = false and write your first article!