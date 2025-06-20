### 🐾 Postman API Testing – Swagger Petstore (Part 2)

This is a continuation of Part 1 which focused on `/pet` endpoints.  
In **Part 2**, the project expands API testing to include the `/user` and `/store` endpoints of Swagger Petstore.

## 🔧 Tools
- Postman & Collection Runner
- Swagger Petstore API (https://petstore.swagger.io)
- Google Sheets (for test case documentation)

## 🧪 Test Scenarios
### 🔹 `/user` Endpoint
- `POST /user` – Create user (valid & invalid)
- `GET /user/{username}` – Retrieve user detail (valid & invalid)
- `PUT /user/{username}` – Update user (valid & not found)
- `DELETE /user/{username}` – Delete user (valid & not found)
- `GET /user/login` – Login user (valid & invalid)
- `GET /user/logout` – Logout user

### 🔹 `/store` Endpoint
- `POST /store/order` – Place order (valid & invalid)
- `GET /store/order/{orderId}` – Get order by ID (valid & not found)
- `DELETE /store/order/{orderId}` – Delete order (valid & not found)
- `GET /store/inventory` – View inventory

## 📜 Test Cases
Full test cases with preconditions and steps:  
[📄 Google Sheet Test Cases](https://docs.google.com/spreadsheets/d/1m4I8VpBhFuYC1Q7w5vk_eQcS7_gt-gLM/edit?usp=drivesdk)

## 📸 Test Results
You can view the collection runner test results here:  
![Screenshot – Collection Runner Result](screenshot/runner-result-collection.png)

## 📝 Notes
- API incorrectly allows login with unregistered user (e.g., invalid email/password inputs still return `200 OK`).
- A `500 Internal Server Error` was encountered on certain invalid updates.

## ⚙️ Setup

1. Clone or download this repository.
2. Open Postman → Import the collection from `./collections/Petstore-V2-Part2.postman_collection.json`.
3. Use the **Collection Runner** or run individual requests manually.
