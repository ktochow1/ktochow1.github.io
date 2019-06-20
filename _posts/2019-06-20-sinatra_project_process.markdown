---
layout: post
title:      "Sinatra Project Process "
date:       2019-06-20 18:23:01 +0000
permalink:  sinatra_project_process
---


Working on my first application was, at first, painfully daunting. Initially, I thought of a Flower Shop Application where a user could create a bouquet using different types of flowers, and then having multiple bouquets with those flowers. So, in this scenario bouquets and flowers would belong_to a user, and users and bouquets would both have_many flowers. My first plan was too complicated for me to follow through and I was adivsed to simplify it. Ultimately I decided to scrap a flowers model and instead created a form to create a bouquet with a text box where a user could type in the name of the flower of their choice. After I simplified my idea creating a skeleton for my project was simple enough. I wrote and drew out how my app should function from a user signing up, to creating content, to logging out. A few hiccups I encountered were making sure that users could not see each other's content, and associating a bouquet with the appropriate customer who created it. Luckily the two worked somewhat together to form a medium hiccup. 
The helper methods which I defined worked to check whether a user was logged in, as well as, check to see if the logged in user was also the same user who's data was being accessed before displaying that data. These helper methods (#current_customer and #logged_in?) were implemented in almost all get controller requests. 
Initially when I created an index form where a user's bouquets were displayed, I made the mistake in iterating through the entire bouquet array. This caused all user's bouquets to be displayed. What I did to fix this was I changed 'Bouquet.all' to '@bouquet = current_customer.bouquets'. The instance variable '@bouquet' needed to be equal to the current_cusotmer 's (helper method) array of bouquets.

The Sinatra App Project was definitely rewarding in the end, I'd only advise you to not work with words like 'bouquet'!
