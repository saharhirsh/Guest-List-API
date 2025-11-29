<<<<<<< HEAD
# Guest-List-API
🎉 Guest List API

A simple Flask-based RESTful API to manage a guest list. This API allows you to add, view, update, and delete guests.

🚀 Features

GET /guests – Retrieve the full guest list.
POST /guests – Add a new guest.
PUT /guests/<guest_id> – Update an existing guest's information.
DELETE /guests/<guest_id> – Remove a guest from the list.
🛠 Technologies

Python 3.x
Flask
JSON for data exchange
📦 Installation

Clone the repository:
   git clone https://github.com/your-username/guest-list-api.git

   cd guest-list-api

Create a virtual environment (optional but recommended):
   python -m venv venv

   source venv/bin/activate  # On Windows: venv\Scripts\activate

Install dependencies:
   pip install -r requirements.txt

Run the app:
   python app.py

📬 API Endpoints

GET /guests

Returns a list of all guests.

Response:

[

  {

    "id": 1,

    "name": "Alice",

    "email": "alice@example.com"

  }

]

POST /guests

Adds a new guest.

Request Body:

{

  "name": "Bob",

  "email": "bob@example.com"

}

Response:

{

  "message": "Guest added successfully",

  "guest": {

    "id": 2,

    "name": "Bob",

    "email": "bob@example.com"

  }

}

PUT /guests/<guest_id>

Updates an existing guest.

Request Body:

{

  "name": "Robert",

  "email": "robert@example.com"

}

Response:

{

  "message": "Guest updated successfully"

}

DELETE /guests/<guest_id>

Deletes a guest by ID.

Response:

{

  "message": "Guest deleted successfully"

}

📁 Project Structure

guest-list-api/

│

├── app.py               # Main Flask application

├── requirements.txt     # Python dependencies

└── README.md            # Project documentation

🧪 Testing

You can test the API using tools like:

Postman
curl
httpie
📄 License

This project is licensed under the MIT License.
=======
# 🎉 Guest List API

A lightweight Flask-based REST API for managing event guest entries. Docker-ready for seamless deployment.

---

## 🚀 Features

- Add new guests with validation
- Retrieve all or specific guests
- Delete guest by ID
- Validates Israeli phone format
- Unique UUID assignment per guest
- In-memory storage with logging

---

## 🐳 Docker Installation

### 1️⃣ Clone the repository
```bash
git clone https://github.com/yourusername/guestlist-api.git
cd guestlist-api
```

### 2️⃣ Build Docker image
```bash
docker build -t giligalili/guestlistapi:ver01 .
```

### 3️⃣ Run container
```bash
docker run -p 1111:1111 giligalili/guestlistapi:ver01
```

API is now running at: `http://localhost:1111`

---

## 📬 API Endpoints

| Endpoint             | Method | Description                             |
|----------------------|--------|-----------------------------------------|
| `/`                  | GET    | Returns unsupported message             |
| `/guests`            | GET    | Lists all guests                        |
| `/guests`            | POST   | Adds a new guest                        |
| `/guests/<id>`       | GET    | Retrieves guest by `seq_num`            |
| `/guests/<id>`       | DELETE | Deletes guest by `seq_num`              |

---

## 📝 Sample POST Payload

```json
{
  "firstname": "John",
  "surname": "Doe",
  "quantity": "2",
  "phone": "0541234567",
  "email": "john@example.com",
  "id": "JD2025"
}
```

---

## ⚠️ Validation Notes

- Quantity must be a positive number.
- Israeli phone numbers: 10 digits, starts with `0`, numbers only.
- `id` must be unique.
- Guest data resets when server restarts (in-memory).

---

## 🛠 Dev Tips

- Logging level is set to INFO.
- You can push updates with:
```bash
docker tag giligalili/guestlistapi:ver01 giligalili/guestlistapi:ver02
docker push giligalili/guestlistapi:ver02
```

---

Let me know if you’d like to extend this project—database integration, front-end dashboard, or even email invitations!
>>>>>>> 0867d20 (added API section)
