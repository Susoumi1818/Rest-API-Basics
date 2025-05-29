# **Day 3: API Versioning, Rate-Limiting, CORS, and Throttling**

**Concepts to Master**

1. **API Versioning**
   Why versioning matters (backward compatibility)
   Common styles: URI versioning (/v1/users), Header versioning

2. **Rate-Limiting**
   Prevent abuse by limiting number of requests per user/IP
   Implement in tools like Postman using environment & delay

3. **Throttling vs Rate-Limiting**
   Throttling: control speed of requests
   Rate limiting: control total number of requests

4. **CORS (Cross-Origin Resource Sharing)**
   Why some frontend apps get "CORS error"
   How APIs allow/disallow certain origins

------------------------------------------------------------------------------------------------------------------------------------

 **Detailed Explanation**

 **API Versioning — Like Updating an App Without Breaking It**

APIs evolve over time to add new features, but many users still rely on old versions. To keep everyone happy and avoid breaking existing apps, developers create multiple API versions.

**Example 1:**
An API v1 shows product name and price.
API v2 adds stock availability, ratings, and reviews.

Instead of forcing all users to upgrade, both versions run side by side:

* `/v1/products` → returns name + price
* `/v2/products` → returns name + price + stock + reviews

✅ Developers choose which version to use based on their needs.

**Example 2: Game Updates**
A game’s v1 lets your car have 3 speeds.
In v2, they add a turbo boost.

Players with older or low-powered devices can stay on v1, while others enjoy new features on v2.
This way, no one is forced out, and nothing breaks.

-------------------------------------------------------------------------------------------------------------------------------------

 **Rate-Limiting — Like a Security Guard at a Buffet**

APIs need to protect themselves from overload or abuse. Rate limiting restricts how many requests a user or app can make in a given time (e.g., 100 requests per minute).

Imagine a buffet where you can only take food 5 times per minute. If you try more, the guard says:

> “Too many visits! Wait before coming again.”

When the limit is hit, the API responds:

```json
{
  "status": 429,
  "message": "Too Many Requests"
}
```

**Why Rate Limiting?**

* Prevents server crashes from too many requests
* Avoids abuse or hacking attempts
* Ensures fair access for all users

The API owner sets:

* How many requests per minute/hour/day are allowed
* Whether limits apply per user, IP, or API key
* The response sent when limits are exceeded

-----------------------------------------------------------------------------------------------------------------------------------

**Throttling — Like a Slow-Speed Lane**

Throttling controls how fast requests come through, instead of blocking them outright.

Back to the buffet:
You can come as many times as you want, but only once every 30 seconds. If you try faster, you have to wait.

**Throttling means:**

> “You can continue, but slowly.”

**Why use Throttling?**

* Prevents users from hammering the server too quickly
* Keeps the system stable during traffic spikes
* Smooths out request flow for all users

-------------------------------------------------------------------------------------------------------------------------------------

**Rate Limiting vs Throttling**

| Feature          | Rate Limiting                      | Throttling                       |
| ---------------- | ---------------------------------- | -------------------------------- |
| What it controls | Total number of requests allowed   | Speed (frequency) of requests    |
| Effect on user   | Blocks requests after limit hit    | Slows down requests, no blocking |
| Example          | Max 100 requests per minute        | Only 1 request every 2 seconds   |
| Response         | HTTP 429 error “Too Many Requests” | Requests delayed or queued       |

-------------------------------------------------------------------------------------------------------------------------------------

**CORS — Cross-Origin Resource Sharing**

When a website tries to get data from a different domain (origin), browsers enforce CORS rules for security.

**Imagine:**
You’re at restaurant `A.com` and bring food from `B.com`. The restaurant manager (browser) says:

> “No outside food allowed unless we have permission!”

Browsers block websites from fetching data from APIs on other domains unless those APIs explicitly allow it.

If not allowed, you get an error like:

```
Access to fetch at 'https://xyz.com/api' from origin 'https://abc.com' has been blocked by CORS policy: No 'Access-Control-Allow-Origin' header is present.
```

**How to Fix CORS:**
The API server must send headers such as:

```http
Access-Control-Allow-Origin: https://abc.com
```

This tells the browser that `abc.com` is allowed to access the API on `xyz.com`.

--------------------------------------------------------------------------------------------------------------------------------------

**What Happens If CORS is Missing?**

* Your frontend app running in browsers cannot read API responses.
* The API works fine, but the browser blocks data for security.
* The user experiences broken functionality or errors in the web app.

*Note: CORS is enforced by browsers only; tools like Postman or curl do not block requests due to CORS.*

--------------------------------------------------------------------------------------------------------------------------------------

**Visual Examples**

**API v2 returns detailed info:**
![API v2 with more details](https://github.com/user-attachments/assets/262fd672-cb51-40ae-8587-cc1c63cae0e7)

**API v1 returns basic info:**
![API v1 with basic details](https://github.com/user-attachments/assets/baf08f47-dae7-46f3-bdd0-048271aba3d9)

