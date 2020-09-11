---
layout: post
title:      "My 4 takeaways from the Rails project"
date:       2020-09-11 00:41:44 -0400
permalink:  my_4_takeaways_from_the_rails_project
---


Here are just a few things that stood out to me while working on my Rails project:
1. Associations - In my Sinatra project, I chose to only have two models, which made associations not as much a concern. However, in Rails, I have four models, and getting the correct associations is crucial.  I had to envision what I wanted the application to do. After deciding what model to make as the join table I was concern about the fourth model. Would it know about users or towns? Ultimately I tried to chose the most direct path from when the user signs in to them leaving a comment.
2. Nested Forms - Can be complex in their implementation. The basic pattern is to create a form_for an object/model and then use a fields_for a second object/model that will be created upon instantiation of the first model/object. Building the form out in the view is pretty straight forward, but for me, it was trying to get the controller actions to know what to do with the incoming information.
3. OmniAuth - I used the bcrypt gem to authenticate my user's login and signup, and I chose Google as my third party signup/login. This blog post was immensely helpful https://medium.com/swlh/google-authentication-strategy-for-rails-5-application-cd37947d2b1b. It gives the step by step process to get set up with Google.
4. Bootstrap - I didn't do a lot of styling in this project. I do plan on revisiting it and focusing on presentation, but for now, I add bootstrap which at the very minimum makes rendered pages look better. This blog helped me to set it up https://medium.com/@biancapower/how-to-add-bootstrap-4-to-a-rails-5-app-650118459a1e.

This project was challenging to say the least. I spent a lot of time researching error methods. One of the common issues I had was when changing a seemingly small line of code in the views, the result would be a controller action error. I've heard that "errors are our friends" and if that's the case then I made lots of new friends.
