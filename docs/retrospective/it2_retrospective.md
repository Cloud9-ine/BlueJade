# Retrospective for iteration 2

## What we have done:
### front end:
function developments:

- Develop CommodityPost page, which can add commodity's name, category, price, photos and description. Also add some rules for those inputs.
- Accomplished the axios request to get data from server and display on the commodity list page.

connecting with backend:

- Upload commodity form and save it into the database.(without photo uploading)

### back end:
Named the back end BlueTrade.

Configured global settings.

Built the Database (files including models.py, settings.py, etc.).

Configured URLs and Provided corresponding APIs to the front end team (the file is urls.py).

Wrote and Debugged the main programs to support basic features of CRUD (View items & Post items in this iteration, files are views.py, search.py, post.py).

Connected the frontend and the backend, testing the features of App. 

## What we have not done:
All tasks we planned for this iteration are accomplished.

## Challenges we have met:

### front end:
Continuously learning Vue.js and other front-end techniques as some of our team members are not familiar with.

### back end:
Connecting the front end and the back end. The front end server and the back end server run locally on different ports, which leads to cross-domain access failure to Django server. After csrf token is added into Restful request, the problem is solved.

## What we want to do in the next iteration:

### front end:
Roughly finish the UserPage, including user info, commodity detail and so on.Finish the commodity management layout in the user page.Update the commodity item page to display the recommendation section.Finish the search feature layout.

### back end:
Change database from sqlite to postgresql for further deployment.

Improved all functions into fully functional, including the post method with pictures.

Basic recommendation system based on Least Recently Used(LRU) cache.

Finish the search features.
