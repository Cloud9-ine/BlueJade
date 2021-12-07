## Problem Statement:
> When newly enrolled students first arrive on the campus, they are always exhausted with purchasing stuff like furniture, daily necessities, electrical devices and so on. Some of them are too expensive to buy for first hand while there exist many graduated students who want to get paid for selling those. However, most students, especially for the international ones, can only contact each other through their own social media or chatting software. Therefore, a university-based platform might be a quite useful solution to solve this real-life problem.

## Potential Clients:
> 
> 1. Enrolled students:
>> those who want to buy stuff before arriving on the campus.
> 2. Graduated students:
>> those who want to sell stuff before leaving the campus.
> 3. (Faculty & Staff, extended to those who have university accounts:)
>> those who work at campus and wish to buy or sell their stuffs
> 4. (Inter-University user groups:)
>> those who want to sell stuff near the campus.

## Proposed Solution:
> A platform for students to view, post, update, remove items for sale or purchasement. Simultaneously, this platform should have broadcast channels and chatting rooms embedded so that users can communicate with each other. Such channels should also support the confirmation for those trades agreed by both sides. Moreover, this platform can have maps and guides embedded so that users can confirm the locations and routes to make a trade.

## Function Requirements:
### Must have:
1. Login: as a potential seller/buyer at Hopkins, I want to be able to login to make a new offer. I want to login with my JHU credential instead of signing up with other information. This function requires an API that request login credential from JHU server.
2. Post: as a seller, after logging in I want to create posts about my offer.
3. Delete post: as a seller, sometimes I don’t want to sell the item I posted any more. It would be nice for me to delete the post I made.
4. Update: as a seller, I want to be able to update my post if anything changes.

5. Search: as a buyer, I want to view all commodities and search them based on keywords.
6. Bookmark: as a buyer, I want to add some interesting commodities to my bookmark for future review.
7. Request trade: as a buyer, I want to leave the message to the seller of some corresponding item with my own "bid".
8. Review bid: as a seller, I want to see all messages left to me with bid so that I can select the highest price from buyers.
9. Confirmation: as a buyer/seller, I want to confirm a trade when an agreement is made.
10. Cancel trade: as a seller/buyer, it would be nice if a user could terminate a confirmation by canceling the trade. Unexpected situations might occur and the user might no longer want to continue the trade. If the buyer decides to cancel a trade, the dealer should decide whether to keep the post as available for trading or archive the post.
11. Contact: as a buyer/seller, I want to get the contact information (email) after the confirmation of the trade so that we can meet afterwards.
12. Notification, as a buyer/seller, I want to get notified once there is any change on my potential trades (like confirmation, offering, bid and so on).

13. Simple recommender system: as a user, I want the app to recommend items that I might be interested in based on my past purchase/browsing history on this app.
14. Account management: as a user, I want to manage my account in the platform so that I can change my password, nickname and other personal information some time in the future.


### Nice to have:
1. Reply to a post: I would like to interact with other users by replying to their post.
2. Direct message: as a seller/buyer, I want to directly message each other and initiate one-on-one conversation.
3. Map: as a seller/buyer, when a trade is confirmed, I want to decide the location for goods exchange and pin the location on a Map so that I can easily find my way to the location.
4. Calendar reminder: as a seller/buyer, I want to have a calendar reminder that reminds me when the trading time is close.

## Software Architecture:
> (Overview) 
>
> Our software still follows the client-server pattern that the clients can use web browsers to do operations on the frontend and the data will be transmitted through requesting and getting responses from the backend. The backend server will conduct logical operations, query the database, get responses and forward information to the frontend. In future iterations, given the more complicated situation like high concurrency, we might introduce load balance into our architecture to assign tasks to several parallel servers.

> (Database) 
> 
> Since our platform requires basic functions including the user login and operations on post, delete, update and view commodity, we will have two databases. One is for the users’ information and the other is for the item’s information.

> (Backend) 
> 
> Each database is an extension of the corresponding interface, which is the user account service and the core commodity service. These two basic kinds of services also belong to their controllers in our backend respectively for the logic operations. For instance, the controller of the login service should handle the authentication process to guarantee the user login is verified correctly. Similarly, the controller of the commodity service should handle the registration of any item such that this post can be identified later correctly. These are then integrated into the application and build the basis of our software’s backend.

> (Frontend) 
> 
> Users of the application can have different relations with the commodity and also other users in future iterations. The frontend first should provide users with basic functions including logging, browsing, getting responses, posting forms, etc.. Also the transmission of information to and from the backend should be supported such that users’ operations can actually have impacts.


