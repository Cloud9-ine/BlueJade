# Retrospective for iteration 4

## What we have done:
### Front end:

We added Leave Message and Make Offer function so that potential buyer can communicate with the seller. A buyer can 
make one offer to a commodity by filling a form with price and message. 

A buyer can see the status of their offer in Profile->My Offers->Your Buying Offers. At the same place the buyer can 
also edit their offer, changing the message or offer price.

We implemented manage goods on userpage. If the user posted any goods for sale, they can edit the commodity 
information or delete post via ManageGoods. A seller can also check if they received any offer via Profile->My 
Offers->Your Selling Offers. The seller can choose whether to accept the offer or not. 

Commodity Item page now is able to display multiple images.

### Back end:
Deploy postgresql on heroku to store user data.

Develop file(images) uploads service with Filestack.

Design commodity recommendation algorithm for users.

## What we have not done:

### Front end:
Three pages in "About Us", security page, avatar page, and the outlook of manage profile page and 
navigation menu. 
We haven't fully implemented edit profile and security (changing email and password). 

### Back end:
Implement different back end APIs at user profile pages, for example, user email validate at security page, Help center page, user avatar page.

## Challenges we have met:

### Front end:

While implementing search item we had issue with invalid commodity showing up in all commodty. We also had trouble 
with navmenu not working properly.

We also had minor issue with displaying image with the correct size.

### Back end:
Because the whole program becomes more sophisticated and lower coupling, it is hard to build our app and API tests locally. Therefore we use postman to send our RESTful APIs with appropriate payloads/parameters/headers. The advantage is we no longer need to build the development environment locally and we can concentrate more on our own work.


## What we want to do in the next iteration:

### Front end:

Finish the layout, design, and features of some subpages in the user profile page: the three pages in "About Us", 
security page, avatar page, and the outlook of manage profile page and
navigation menu.
we also want to fully implement edit profile and security (changing email and password).

Create a common 404 page for the application.

Update the commodity item page to display the recommendation section.

Incorporate the authentication to routing

### Back end:
Build and complete user bidding system, promote communications between sellers and buyers by leaving necessary information with each other.

Implement user login and register.

