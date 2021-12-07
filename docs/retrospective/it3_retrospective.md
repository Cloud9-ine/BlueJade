# Retrospective for iteration 3

## What we have done:
### Front end:

Finish the search feature layout.

Roughly finish the UserPage, including user info, commodity detail and so on.

Roughly finish the commodity management layout in the user page.


### Back end:
Formally add CRUD APIs to the back end and corresponding templates for testing.

Deploy our back end program on Heroku and it can be accessed remotely, which is convenient for front end testing.

Merge the confusing READMEs into one README with appropriate user guides.

Accept an image uploading for POST which will store locally on the server.

## What we have not done:
Update the commodity item page to display the recommendation section.

## Challenges we have met:

### Front end:

Because of the deployment issue, found it hard to test with the real-time data.

Continuously learning Vue.js and other front-end techniques as some of our team members are not familiar with.


### Back end:
Deploying programs to Heroku as expect is challenging. We often get 403 Forbidden error from the server because Django server thinks it might be a cross-site forgery. It is solved after we unregister the csrfmiddleware of Django.

## What we want to do in the next iteration:

### Front end:

Finish the layout, design, and features of some subpages in the user profile page: such as my profile, my avatar, manage goods, and security.

Create a common 404 page for the application.

Update the commodity item page to show real-time data and routing from the commodity list page.

Update the commodity item page to display the recommendation section.

Incorporate the authentication to routing


### Back end:
Chat system that support instant messaging to help user and buyer exchange their information. 

Finish the basic recommendation system.

Information storing on the back end by connecting to database.