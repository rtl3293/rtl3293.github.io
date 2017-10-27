---
layout: post
title:      "'Pry'm to Debug!"
date:       2017-10-27 04:54:13 +0000
permalink:  prym_to_debug
---


So I had my first big debugging sesh while working on the Sinatra ActiveRecord Crud Lab. I was using Ruby 2.4.2 in my local environment running on my MacBook Pro and after looking thoroughly through my code I couldn't find **ANYTHING WRONG!** I kept receiving the same error message, 
```1) Blog Post App Create Action creates a new blog post
     Failure/Error: expect(Post.last.name).to eq("my favorite blog post")
     
     TypeError:
       Cannot visit Integer```
			 
It was infuriating. But I knew it was time to dig in. So, after making a couple google searches for the error message and only seeing articles that were unrelated to sinatra, it was time to try a screenshare. 

I get into the screenshare with Scott and we're running my code and everything looks like it should be working fine. But again, we run #Post.last and #Post.first and we receive that SAME error. That's when they decided to pull my code down onto their machine and try it out on their system. 

BOOM!

It works there. Now we were onto something. We discovered that he was running Ruby 2.3.1, while I was on 2.4.2. So now it was time to rememeber how to use RVM again. After a bit more of googling and working with Scott on remembering how to use RVM, we got my machine switched to 2.3.1. After reinstalling bundler and the gems in my gemfile, we did it! It passed all the tests, and I was good to move on. 

This was easily one of my favorite labs I've worked on throughout the bootcamp so far, because it was my first real issue I've had to deal with in my local environment that had to with code I **DIDN'T** write. It gave me what I expect is a little taste of the real world. Code is fun that way, sometimes it's the smallest detail that can make or break a project. 
