---
layout: post
title:      "Lessons Learned - My Rails Portfolio Project"
date:       2018-03-10 22:16:12 +0000
permalink:  lessons_learned_-_my_rails_portfolio_project
---


As I was going through the Rails curriculum, I kept thinking, “Man, I need more exercises on that.”  I proceeded knowing that with each lab Rails would feel less foreign and magical to me.  I was right, however, I sure was glad to get to the final Rails project and have a chance to put all the parts together.  Below are my takeaways.

1. Naming is a pain.  I named my join table attendee and I hate it.  Either you have attendees or you are an attendee, but as I was writing the code, the name just didn’t flow.  I did look at different ways to refactor, but in the end decided that would be a big chunk of time that resulted in me, not the end-user, benefitting.  
1. Using aliases can be very helpful when you have a user model with different roles. 
1. I am prone to say, “I bet there is an app for that.” Now, I can say, “I bet there is a method for that.” Ruby, Rails, Devise, Pundit all have methods to make our lives easier, you just have to find them.  
1. Customizing Devise can be done.  It just takes time - reading the documentation and searching Stack Overflow. The following helped me:
* #update_resource - allows user to update information without a password if they are signed in through Omniauth.  This was really helpful to me since my users needed more than an email and password.   
* #after_update_path_for and #after_sign_in_path_for – Help customize where devise sends the user.
1. I still need some work with RESTful paths.  My biggest concern is when it is acceptable to deviate.  I have a model StudySession.  I want to show it, but differently depending on what type of user is viewing it.  I did this by making different partials as well as a controller for the join model, Attendee.  I wonder, however, if making a controller for different users would have been better/just as good.  I did make a controller for Admin.  
1. Making it pretty takes time.  I spent one day just on adding Bootstrap and laying out my very simple web app.  I am going to look back at that video in the curriculum where Avi is like, “Oh, I like this layout. I’ll just take their CSS.” Then, poof, he had copied one or two files and his web app looked like theirs.  This did not seem as easy for me as for him.  I did not even get around to changing the fonts on mine.  
1. Something so simple, yet crucial is that dotenv gem has a rails version dotenv-rails. 


I would still say the hardest part of this project is the architecture of the web app - How do you want to setup your database? What names and associations do you want to have for your models?  Which controllers and views do you use for what you want your user to be able to do?  I spent more time pondering these decisions than I did coding.  The daunting part to me is that there is no right answer out therefor you to find.  You have to make the decisions and after a time, live with them.  

There are still things that I would like to do with this web app.  I would like to expand the capabilities of Admin. I would really like to have them set the role for each user as well as update each user.  They should also be able to create study sessions, but I would need to add more options into the view or refactor my #create in that controller.  After writing this, I am going to go back and ponder the route I am using for my student user to view their own study sessions.  I think, perhaps, I should use another partial instead of the join table controller.

My app is missing something BIG – the tests!  I started out trying to be good, but ended up doing what many probably do, just getting it to work.  I need to go back and write tests.  This exercise would help me learn more about tests as well as test the functionality of my program.  This is where my student dashboard that says I haven’t programmed in days and my lesson/week is 0 really does not benefit the learning process.  I want to move forward, but at some point I really need to standstill and take a look around!

This project can be found at https://github.com/efl7a/come-on-in.git

