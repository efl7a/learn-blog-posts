---
layout: post
title:      "The Making of a My First React App – Queen City Rezoning"
date:       2018-09-19 20:23:37 +0000
permalink:  the_making_of_a_my_first_react_app_queen_city_rezoning
---

The idea – I want an app where I can see the rezoning petitions in my area.  Our county government has such a site, but it doesn’t give enough information in my opinion.  This app should scrape the current website, then allow users to search and add comments related to the petitions.  It would be great if I could eventually link Google maps with an estimated location.
Beginnings – First, I am going to create a rails api using the instructions from[ here](https://www.fullstackreact.com/articles/how-to-get-create-react-app-to-work-with-your-rails-api/).  I am mainly concerned with my database here.  After set up, I am going to use part of the code from my CLI gem (Object Oriented Ruby final project) to seed the database.  
Then I will use create-react-app to set up the client side.

**Lingering Questions:**
1. How do other apps keep their database up-to-date?  Do they update the database every time a user logs in or is it a timed event?
2.  How likely is it that the comment section will erode rapidly into chaos without forcing people to login before commenting?

**Lessons Learned:**
1.  The Joy of Git
 When I got the basic functionality of my web app completed (even a little before to be honest), I wanted to experiment with other options like a sorting button or navigation bar.  This is where I love git’s branching ability.  I could work on different options in different branches.

Git commands to know:

git co -b [new-branch-name]

git push origin [new-branch-name]

At one point I was having some serious difficulty with a main feature of my base app, the ability to persist (POST) new comments.  When I was frustrated with this feature, I created a new branch and focused on a different feature, sorting by number or by district.  It was a nice break and allowed me to have some wins.  During this, however, I still tinkered with the persisting code.  I was able to get it to work and then had to figure out how to catch my branch up with master.  
Git command to know:

git merge master (while in the branch directory)  

2.  I need more information on norms.  A question came up about whether to use fetch and let the backend do some sorting/finding or do I just use the current state and use JavaScript.  I think you should use the api, but it was easier (faster during development) to us JS.  

**Still Working:**
1.	Add/use bootstrap to make it look nicer.
2.	Having users sign in.
3.	Adding google maps.
4.	Learning how to launch an app.

