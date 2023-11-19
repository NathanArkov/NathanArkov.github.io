---
layout: post
title:  "Linux commands 101"
date:   2023-10-31
featured_image: 2023-10-31-make-your-own-media-server/blog-thumbnail.png
tags: [Linux, Cheat-Sheet]
---

Just a random list of useful Linux commands I use often.

#### List files
`ls [args]`

list files in a directory 
`ls`

show ownership of files
`ls -l`

#### Copy
`cp [source] [dest]`

copy file1 into file2 `cp file1 file2`

#### Move 
`mv [source] [dest]`

move file from dir1 to dir2 `mv dir1/file dir2/file`

rename file1 into file2 `mv file1 file2`

#### Remove
`rm [args]`

delete file `rm file`

delete entire directory and its files `rm -rf dir/`

#### APT
`apt [args]`

update package repositories `apt update`

update packages `apt upgrade`

remove package `apt remove package1`

#### Firewall
##### UFW
`ufw [args]`

enable ufw `ufw enable`

disable ufw `ufw disable`

show status / rules `ufw status (verbose)`

add a rule `ufw allow-/-deny port`

add a rule only for TCP `ufw allow-/-deny port/tcp`

add a rule only for UDP `ufw allow-/-deny port/udp`

##### IPTABLES