---
layout: post
title:      "Rails with JQuery Front End"
date:       2018-05-15 21:17:25 +0000
permalink:  rails_with_jquery_front_end
---



Let me lead with - I have really enjoyed this program so far.  Now, why in the world could we not use remote: true in this lab?  Every google question I asked was answered with remote :true.  Through perserverence and a lot of time, a web page I am happy with.  Because of this project I feel a lot better about JavaScript and JQuery.  

On to lessons learned.  First, the most mysterious thing for me was rendering forms with an AJAX call.  At first, I spent time and just recreated the form for the edit action.  For new, I cheated and put the form in the original page, but hid it upon page load.  I really felt like this was cheating, so I spent quite a lot of time searching for the "right" way.  I never found it.  However, I did (after many searches) find:

`render layout: false`

I might have learned this earlier, but had forgotten it or more correctly did not associate this capability with using Rails as an API.  That is something these projects help you with, consolidating your knowledge.

Second, there is still lots to learn regarding cacheing and click events.  I have found that sometimes it takes two clicks before the expected action happens.  More often than not a desired action happens multiple times.  This was true for an alert attached to my Delete buttons:

`<%= button_to "Delete Study Session", "#", :method => 'delete', :data => {confirm: "Are you sure?", id: study_session.id}, form_class: "teacher", class: 'btn btn-danger btn-xs' %>`

Why does it fire 2 or 3 times? 

Finally, maybe I should have called this - So many lessons to learn.  I still have so much to do.  I did not change my admin section, so it is currently not working due to the changes I made in the controller.  I did not make a JS class object, because I didn't see the point in my case.  If can do all the CRUD events with AJAX and persist changes, why would I create a JS object? This is definitely an area that I need more input from others.  I have not been able to find internet answers that convince me that there is a standard or best practice.  I think there is, but I have not found it *unless* it is remote: true!



