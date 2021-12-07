Code Review (Group 3)

Design:

-Front end:

The structure of our code is consistent with the functions we implemented. We are following the single responsibility principle such that each class has only one responsibility. 


-Back end:

The code in the backend is appropriate with our system. And we are following the single responsibility principle and the open-closed principle. We keep functions as simple as possible and make sure they are only responsible for one thing. Besides, we keep existing code from breaking when we implement new features in different iterations.


Complexity:

-Front end:

Some Vue files have duplicate code related to css style. We have tried to simplify them, but still left some.
We uniformed the style by writing an additional style javascript file, which makes our code clean and simple. Also, we set up axios, global parameters, backend urls and some other settings in the main.js file, which makes our code readable and decoupled.


-Back end:

Similar to the front end codes, there are also duplicate codes in back end programs. Most of them are generated as a result of inconsistency during testing APIs themselves. We also tried to reduce the duplicate codes as far as we could. Still, we kept some duplicate codes.
During the development, we try to separate classes and functions into different modules so that we can reduce the coupling. This part is still readable and easily extended in the future after this code review.


Naming:

-Front end:

Each variable, class, file, and method has a clear name. The naming reflects properties or functionalities of the variable. We follow the Camelcase and Pascalcase naming conventions in our code.


-Back end:

We follow the Python naming style with all class names in Camelcase and all function names in UnderScorecase. All names consist of meaningful phrases like search_commodity_by_id and short, confusing variable names are avoided.


Comments:

-Front end:

There are just enough comments for the front-end codes, however, more comments should be included for better maintenance consideration in the future. In addition, some commented lines are not used but are still displayed, maybe try to eliminate those unused commented code if necessary.


-Back end:

There are some comments for the backend code when developing. However, in the code review process, some comments were duplicate so we deleted them, and some essensial comments were missing, so we added some to increase code readability.  Comments are enough for most APIs, especially their corresponding URLs, indicating how one API can be used and what links and parameters it needs. Also, there are some commented codes during testing the functions of APIs, we may delete them in the end.


Style:

-Front end:

The code style is unified and consistent. We follow the Camelcase and Pascalcase naming conventions in our code. Methods and classes are kept short and have only corresponding responsibility. Duplicate code is avoided. Data clumps are compressed into json data.


-Back end:

We keep our back end code with python style PEP 8. We use camelcase for all class names and underscorecase for all function names. All functions are separated with two lines, and we successfully avoid some bad code smells like large class or data clumps. However, we still retain some duplicate code in functions which can be extracted as external supporting functions. In addition, we still have some duplicate primitive terms in our data models. It is hard to refactor them now because it might bring changes to our existing databases and all back end logic and require heavy work.


Documentation:

There is a readme file to explain how to install and use the application. However, more detailed explanations could be added, and also provide some user cases and demo accounts for better understanding.
