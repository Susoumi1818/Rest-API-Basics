DAY 2

Path Parameters
The path variable comes immediately after a slash in the path. 
You can have multiple path variables in a single request, such as this endpoint for getting a user's GitHub code repository:

Use Query Parameters
Query Parameters (start after ?)​- These are filters or custom settings for the API to narrow down what you're asking.
Example: I need users from mockapi/employees  system using version 2 of the API that should only contain users with status as active
​
![image](https://github.com/user-attachments/assets/dc78da1b-89e8-4cb3-8c11-f6c8db5c8396)


#GET
curl --location 'https://68355401cd78db2058c0f896.mockapi.io/api/v2/employees/Users?status=Active' \
--data ''
Response:
[
    {
        "Name": "Name 3",
        "email": "sushho.mee@me",
        "role": "Architect",
        "status": "Active",
        "id": "3",
        "name": "Susoumie"
    }
]

Screenshot #GET
![image](https://github.com/user-attachments/assets/bdf867a6-4a3b-4028-9456-bb1d7dd2332c)


Validate Status Codes
In Postman: Make sure 
POST returns 201 Created
GET returns 200 OK
DELETE returns 200 OK or 204 No Content

Handle 4xx for incorrect requests

The 401 (Unauthorized) status code indicates that the request has not been applied because it lacks valid authentication credentials for the target resource
The 403 (Forbidden) status code indicates that the server understood the request but refuses to authorize it403 error can result when a user has logged in but they don't have sufficient 
privileges to access the requested resource. E.g. normal employee trying admin rights

Response Codes:

2xx
200 - OK
201 - Created
204 - No content (silent OK)

3xx
301 - Moved (path changed)

4xx
400 - Bad request
401 - Unauthorized
403 - Not Permitted
404 - Not Found
429- Rate limit exceed
418- server’s limitation

5xx
500 - Internal server error
502 - Bad gateway
504 - Gateway timeout

Collection: https://test99-9907.postman.co/workspace/test-Workspace~ccf9b5bf-475f-4039-8c0a-ae740e6757a2/collection/36804728-44001c5b-a6fc-4326-94f3-ab6f62e65273?action=share&creator=36804728&active-environment=36804728-1d605311-1a88-4558-b76b-9930ee4bd529

