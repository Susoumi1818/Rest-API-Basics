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

--------------------------------------------------------------------------------------------------------------------------------------

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


