
# 📧 Email Writer Backend (Spring Boot)

This is the backend service for the **Email Writer** application. It uses Spring Boot to expose a REST API endpoint that takes in email content and a desired tone, and generates a response email accordingly using a service logic (can be extended to use AI or templates).

---

## 🚀 Features

- Accepts POST requests with email content and tone.
- Returns a generated email response.
- Cross-Origin support enabled (`CORS: *`).

---

## 📦 Tech Stack

- Java 17+  
- Spring Boot  
- Lombok  
- Maven  

---

## 🛠 Project Structure

```

com.email.writer.app
│
├── EmailGeneratorController.java   // REST Controller
├── EmailGeneratorService.java      // Service logic to generate email
├── EmailRequest.java               // DTO for request body

````

---

## 🔗 API Endpoint

### `POST /api/email/generate`

Generates a reply to an email.

#### ✅ Request Body (JSON):
```json
{
  "emailContent": "Dear John, I hope this message finds you well...",
  "tone": "formal"
}
````

#### 📬 Response:

```
"Dear John, Thank you for reaching out..."
```

---

## ▶️ Running the App

1. **Clone the repository**

   ```bash
   git clone https://github.com/ThisIsSumit/Smart-Email-Writer-Backend.git
   cd Smart-Email-Writer-Backend
   ```

2. **Build the project**

   ```bash
   mvn clean install
   ```

3. **Run the Spring Boot application**

   ```bash
   mvn spring-boot:run
   ```

The application will start on [http://localhost:8080](http://localhost:8080)

---

## 🌐 Cross-Origin Resource Sharing (CORS)

The application is configured with:

```java
@CrossOrigin(origins = "*")
```

to allow requests from any frontend domain. Change this in production for better security.

---

## 📄 Example cURL

```bash
curl -X POST http://localhost:8080/api/email/generate \
-H "Content-Type: application/json" \
-d '{"emailContent": "Hello team, I want an update on the project status.", "tone": "polite"}'
```

---

## 👨‍💻 Author

Sumit Kumar
[GitHub](https://github.com/ThisIsSumit)
[LinkedIn](https://www.linkedin.com/in/sumit-kumar-a6a69825a/)

---



