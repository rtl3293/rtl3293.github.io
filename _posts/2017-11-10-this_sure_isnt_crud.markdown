---
layout: post
title:      "This sure isn't "CRUD""
date:       2017-11-11 03:36:03 +0000
permalink:  this_sure_isnt_crud
---


Working with Sinatra and ActiveRecord helped me learn a lot. Working with a CLI is great, but everyone wants to be on the web. Building my first web app made me feel like I actually made it. 

Building my routes by following REST, helped my build an app that is understandable, and easy to follow. It also helped me to make it more dynamic. 

Thanks to the 'bcrypt' gem, I was able to implement user(coach) authentication that encrypeted the user's password with a password_digest column in the table, and calling #authenticate when authenticating the user. This method is part of my user class due to me including has_secure_password macro inside it. 

The biggest thing I learned was planning is everything. I started with an idea, but the first night sitting at my computer I basically just stared at it and didn't know where to start. That's when I ended up just sitting and using my notebook to actually schedule how I wanted everything to work. That made the process afterwards much easier to actually implement. 


