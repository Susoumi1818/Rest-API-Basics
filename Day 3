**Day 3: API Versioning, Rate-Limiting, CORS, and Throttling**
**Concepts to Master**

1) **API Versioning**
Why versioning matters (backward compatibility)
Common styles: URI versioning (/v1/users), Header versioning

2) **Rate-Limiting**
Prevent abuse by limiting number of requests per user/IP
Implement in tools like Postman using environment & delay

3) **Throttling vs Rate-Limiting**
Throttling: control speed of requests
Rate limiting: control total number of requests
CORS (Cross-Origin Resource Sharing)
Why some frontend apps get "CORS error"
How APIs allow/disallow certain origins

------------------------------------------------------------------------------------------------

**Explanation of the API Versioning, Rate-Limiting, CORS, and Throttling in detail**

**API Versioning — Like Updating an App Without Breaking It**
Need of versions.

Example 1
For example, we have an app which shows the the Product on your app
Suppose we have an API version 1 V1 which allows you to see Product name and price
Now in API version 2 V2 , the system shows you Product name, price , stock availability, ratings, and reviews.
Some users want to stay in V1 and some want V2
Instead of changing the framework of API, we create 2 separate versions
Instead of forcing everyone to use the new version (which could break older apps), the backend keeps both:
/v1/products → just name + price
/v2/products → name + price + stock + reviews
✅ Developers can choose what they want based on how much detail they need.


Example 2
Game Updates
Imagine you're playing a game like “Car Racer 1”.
In v1, your car has 3 speeds.
In v2, they added a turbo boost.
But some players like the old way, or their phone can't handle turbo.
So:
v1 remains for lightweight phones
v2 is available for new phones with more power

✅ Keeps both audiences happy, and nothing breaks!

**Rate-Limiting**
Rate limiting ensures that a user, app, or IP address can only make a certain number of requests in a given time window (like 100 requests per minute). APIs can be expensive to run. Limits save money. It ensures all users get a fair chance to access the data. 
Too many requests = overload = crash!!!

It’s like setting a speed limit on a road — not to stop you, but to protect everyone from accidents.
For example, Suppose a person is taking food every 5 seconds. You can only come 5 times per minute.

Response
{
  "status": 429,
  "message": "Too Many Requests"
}
**Rate Limiting = "You’ve hit your limit. No more requests."**

The API developer who owns the API creates the API rate limit. They decide
decide:
How many requests per minute/hour/day are allowed.
Whether limits apply per user, per IP, per API key, etc.
What response to send if the limit is crossed

-----------------------------------------------------------------------------------------------

**Throttling** 
Throttling manages the speed of your work and the number of requests you can make in a second.
Manage traffic smoothly.
You can go to the buffet, but only once every 30 seconds.
For example, You’re allowed unlimited visits, but only once every 10 seconds.

**Throttling = "You can continue, but slowly."**
Why APIs Use Throttling:
Prevent users from hammering the server too fast
Keeps the system stable and fair for all users
Helps avoid server overload in high traffic situations

You are not blocked in Throttling, unlike Rate Limit, but you are slowed down.

Real-World API | Rate Limit vs Throttling Example:
✅ 100 requests per minute (Rate Limit)
🐢 Only 1 request every 2 seconds (Throttle)
So:
If you send more than 1 request per 2 seconds, it gets delayed or queued.
If you send more than 100 requests in a minute, you get blocked with 429 error.

-----------------------------------------------------------------------------------------------

**CORS = Cross-Origin Resource Sharing**

When your website tries to fetch data from a different origin, browsers protect users by blocking these requests unless the other site explicitly allows it. A browser security rule that blocks calls across domains. The Browsers enforces it, not servers.

You're at a restaurant A.com You bring in food from restaurant B.com
The restaurant manager (your browser) says:

“Hey! You can’t bring food (data) from another place unless we’ve been told it's okay.”
That’s CORS in action.

You fetch data from an API, and the browser says:❌ “Access to fetch at 'https://xyz.com/api' from origin 'https://abc.com' has been blocked by CORS policy.”

It means the API at xyz.com has not given permission to abc.com to access it.

Error response: CORS policy: No 'Access-Control-Allow-Origin'
How to fix CORS?	Add CORS headers on the API side to allow specific domains

If CORS is missing or misconfigured, your frontend app won’t be able to use the API response in browsers, causing functionality to break, even though the API itself works fine.
-----------------------------------------------------------------------------------------------

V2 with humid details
![image](https://github.com/user-attachments/assets/262fd672-cb51-40ae-8587-cc1c63cae0e7)

V1 with watertemp details as well
![image](https://github.com/user-attachments/assets/baf08f47-dae7-46f3-bdd0-048271aba3d9)


