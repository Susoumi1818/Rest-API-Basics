# Rest-API-Basics
Day 1 Rest API Basics
#Endpoints Used
GET- Used to fetch/retrive data
POST- To create new data
PUT- to whole record
PATCH- to update certain records
DELETE- to surgically remove data

Samples from https://mockapi.io/projects/68355401cd78db2058c0f897

#GET
curl --location 'https://68355401cd78db2058c0f896.mockapi.io/api/v2/employees/Users'

Response:
[
    {
        "0": {
            "id": 1,
            "name": "John Doe",
            "email": "john.doe@example.com",
            "role": "Developer",
            "status": "Active"
        },
        "1": {
            "id": 2,
            "name": "Jane Smith",
            "email": "jane.smith@example.com",
            "role": "Designer",
            "status": "Active"
        },
        "2": {
            "id": 3,
            "name": "Alice Johnson",
            "email": "alice.johnson@example.com",
            "role": "Manager",
            "status": "Inactive"
        },
        "3": {
            "id": 4,
            "name": "Bob Brown",
            "email": "bob.brown@example.com",
            "role": "Developer",
            "status": "Active"
        },
        "4": {
            "id": 5,
            "name": "Charlie Black",
            "email": "charlie.black@example.com",
            "role": "Marketing",
            "status": "Active"
        },
        "5": {
            "id": 6,
            "name": "Diana White",
            "email": "diana.white@example.com",
            "role": "Support",
            "status": "Inactive"
        },
        "Name": "Name 1",
        "email": "email 1",
        "role": "role 1",
        "status": false,
        "id": "1"
    },
    {
        "0": {
            "id": 82,
            "name": "Susoumie",
            "email": "sushho.mee@me",
            "role": "Architect",
            "status": "Active"
        },
        "Name": "Name 2",
        "email": "email 2",
        "role": "role 2",
        "status": false,
        "id": "2"
    },
    {
        "Name": "Name 3",
        "email": "sushho.mee@me",
        "role": "Architect",
        "status": "Active",
        "id": "3",
        "name": "Susoumie"
    }
]

Screenshot Get Method
![image](https://github.com/user-attachments/assets/ffca6b72-cdec-40c3-8333-fa8bda601678)


#POST
curl --location 'https://68355401cd78db2058c0f896.mockapi.io/api/v2/employees/Users' \
--header 'Content-Type: application/json' \
--data-raw '    {
        "id": 823,
        "name": "Susoumie112",
        "email": "sushho.mee@me1112",
        "role": "ArchitectLove",
        "status": "Active"
        }

Response
{
    "Name": "Name 4",
    "email": "sushho.mee@me1112",
    "role": "ArchitectLove",
    "status": "Active",
    "id": "4",
    "name": "Susoumie112"
}
Screenshot POST Method
![image](https://github.com/user-attachments/assets/38e45f7d-ebe1-4422-8a84-3134642139db)



#DELETE 

curl --location --request DELETE 'https://68355401cd78db2058c0f896.mockapi.io/api/v2/employees/Users/4'

Response:
{
    "Name": "Name 4",
    "email": "sushho.mee@me1112",
    "role": "ArchitectLove",
    "status": "Active",
    "id": "4",
    "name": "Susoumie112"
}
Screenshot Delete method:
![image](https://github.com/user-attachments/assets/dc696fc3-30a0-4dc6-a67a-bde1f3477bf9)


#PATCH
curl --location --request PATCH 'https://68355401cd78db2058c0f896.mockapi.io/api/v2/employees/Users/4' \
--header 'Content-Type: application/json' \
--data '{
    "role": "Architect245"
}'

Response
{
    "Name": "Name 4",
    "email": "sushho.mee@me1111",
    "role": "Architect245",
    "status": "Active",
    "id": "4",
    "name": "Susoumie111"
}


Screenshot Patch Method
![image](https://github.com/user-attachments/assets/7d0551ee-8380-4f68-a47a-18fc0abf5446)

Exaplanation:
GET: Fetches list of users
POST: Creates a new user
PATCH: Updates user partially
DELETE: Removes user by ID

Day 1 - Rest APIs Basic
