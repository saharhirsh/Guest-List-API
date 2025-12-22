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
docker build -t saharhirsh/guestlistapi:ver01 .
```

### 3️⃣ Run container
```bash
docker run -p 1111:1111 saharhirsh/guestlistapi:ver01
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
docker tag saharhirsh/guestlistapi:ver01 saharhirsh/guestlistapi:ver02
docker push saharhirsh/guestlistapi:ver02
```

---
