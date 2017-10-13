---
layout: post
title:      "CLI Data Gem"
date:       2017-10-13 00:53:53 +0000
permalink:  cli_data_gem
---


Building my CLI data gem was a lot of fun. It let me take a lot of what I've learned in Ruby and create something that actually meant something to me. I built a ruby gem that scraped a website I visit called The Fader, it then aggregated the articles based off of a category the user chose, and shows them the article titles, as well as description for the article. It then allows the user to choose an article to open and read in their browser using the Launchy gem. 

## CLI.rb

### #call

I first created my CLI controller. The first method I created was my .call method. This method initializes my CLI. This method takes in no arugments, and only calls two methods. The #list_categories method, and the #menu method.


### #list_categories

Next we have my #list_categories method. This method uses the class variable categories to loop through the array to display the options for the user.

### #menu

The next method is the #menu method. This is where most of the user interaction comes in. This method first takes in the user input for which category they would like to see. After checking which category, it creates a new Scraper object and calls the #scrape_page method on it. It passes in an agrument bassed on @@category and the user input. This creates and returns an array with each article as an object.

## Scraper.rb
I created the Scraper class to have a class constant of the url of the homepage we are scraping.


Now we get to the nuts and bolts of actually scraping our website. The .scrape_page class method takes in an argument that is the end of our url that the user wants to see. We use the open-uri gem to save the html as a file we can use, we then use nokogiri on it to make it into parsable data. After a lot of testing and manipulation, I found the CSS selectors that worked best to grab each article I wanted to use, and then collected them into an array that included a hash for each article that includes the articles title, description, and link to it. 

The .scrape_trending_page works almost exactly the same way, but has some slightly different CSS selectors. It also needed to check for blank input, due to the website having empty cards that used the same selectors as the articles.


# What I Learned

Working on this project was amazing. I used Object Oriented design principles to create an entire program out of different kinds of objects that I created and designed. This allows my code to be as clean and concise as possible. I had a lot of fun building this from a simple framework that showed off what I wanted to do, all the way into a program that is built from different objects and manipulates those objects to do everything.  





