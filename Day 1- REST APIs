# Rest-API-Basics

**Day 1 Rest API Basics**
Understanding API
**What is an API ?​**
API stands for Application Programming Interface.​
Imagine you’re at a restaurant:
You are the customer.​
The kitchen is the system that prepares your food.​
The waiter is the API.​

​**Real Life Example​**:
You look at a menu and say, “I want butter chicken.”​
The waiter takes your order to the kitchen.​
The kitchen prepares the food and gives it to the waiter.​
The waiter brings the food back to you.​
➡️ You never talk directly to the kitchen. You talk to the waiter (API).​

**Technical Example:**​
Let’s say you’re using a mobile app to check the weather:​
You (User) tap “Check Weather.”​
The app sends a request via an API to the weather service.​
The weather service (like a kitchen) prepares the data (temperature, forecast).​
The API (waiter) brings that data back to your phone.​
✅ You get to see the weather in seconds — without needing to know how it works behind the scenes.​

**Key HTTP Methods (Use Like a Pro)​**
GET: Fetches list of users
POST: Creates a new user
PUT: Updates whole data record
DELETE: Removes user by ID
PATCH: Updates user partially

**JSON: The API Language​**
JavaScript Object Notation (JSON) is the standard API data format.​
Why?​
1) Key-value based: simple to understand. Label the actual data. We write what we think. JSON readable both for humans and machines​
2) Lightweight and easy to parse: JSON is small in size, uses less data, and is fast to send/receive over the internet.​
3) Language-independent: JSON can be understood and used by almost any programming language.​

## ⚙️ HTTP Methods

| Method  | Action                     |
|---------|----------------------------|
| GET     | Fetch data                 |
| POST    | Create new resource        |
| PUT     | Update whole resource      |
| PATCH   | Partially update resource  |
| DELETE  | Delete resource            |

---

## 🧪 API Endpoint Used

Base URL:  
`https://68355401cd78db2058c0f896.mockapi.io/api/v2/employees/Users`


Samples from https://mockapi.io/projects/68355401cd78db2058c0f897

**#GET**
curl --location 'https://68355401cd78db2058c0f896.mockapi.io/api/v2/employees/Users'

**Response:**
[{"0":{"id":1,"name":"John Doe","email":"john.doe@example.com","role":"Developer","status":"Active"},"1":{"id":2,"name":"Jane Smith","email":"jane.smith@example.com","role":"Designer","status":"Active"},"2":{"id":3,"name":"Alice Johnson","email":"alice.johnson@example.com","role":"Manager","status":"Inactive"},"3":{"id":4,"name":"Bob Brown","email":"bob.brown@example.com","role":"Developer","status":"Active"},"4":{"id":5,"name":"Charlie Black","email":"charlie.black@example.com","role":"Marketing","status":"Active"},"5":{"id":6,"name":"Diana White","email":"diana.white@example.com","role":"Support","status":"Inactive"},"Name":"Name 1","email":"email 1","role":"role 1","status":false,"id":"1"},{"0":{"id":82,"name":"Susoumie","email":"sushho.mee@me","role":"Architect","status":"Active"},"Name":"Name 2","email":"email 2","role":"role 2","status":false,"id":"2"},{"Name":"Name 3","email":"sushho.mee@me","role":"Architect","status":"Active","id":"3","name":"Susoumie"}]

**Screenshot Get Method**
![image](https://github.com/user-attachments/assets/ffca6b72-cdec-40c3-8333-fa8bda601678)


**#POST**
curl --location 'https://68355401cd78db2058c0f896.mockapi.io/api/v2/employees/Users' \
--header 'Content-Type: application/json' \
--data-raw '    {
        "id": 823,
        "name": "Susoumie112",
        "email": "sushho.mee@me1112",
        "role": "ArchitectLove",
        "status": "Active"
        }

**Response**
{
    "Name": "Name 4",
    "email": "sushho.mee@me1112",
    "role": "ArchitectLove",
    "status": "Active",
    "id": "4",
    "name": "Susoumie112"
}
**Screenshot POST Method**
![image](https://github.com/user-attachments/assets/38e45f7d-ebe1-4422-8a84-3134642139db)



**#DELETE** 

curl --location --request DELETE 'https://68355401cd78db2058c0f896.mockapi.io/api/v2/employees/Users/4'

**Response:**
{
    "Name": "Name 4",
    "email": "sushho.mee@me1112",
    "role": "ArchitectLove",
    "status": "Active",
    "id": "4",
    "name": "Susoumie112"
}
**Screenshot Delete method:**
![image](https://github.com/user-attachments/assets/dc696fc3-30a0-4dc6-a67a-bde1f3477bf9)


**#PATCH**
curl --location --request PATCH 'https://68355401cd78db2058c0f896.mockapi.io/api/v2/employees/Users/4' \
--header 'Content-Type: application/json' \
--data '{
    "role": "Architect245"
}'

**Response**
{
    "Name": "Name 4",
    "email": "sushho.mee@me1111",
    "role": "Architect245",
    "status": "Active",
    "id": "4",
    "name": "Susoumie111"
}


**Screenshot Patch Method**
![image](https://github.com/user-attachments/assets/7d0551ee-8380-4f68-a47a-18fc0abf5446)

**Explanation:**
GET: Fetches list of users
POST: Creates a new user
PATCH: Updates user partially
DELETE: Removes user by ID

**Day 1 - Rest APIs Basic**
