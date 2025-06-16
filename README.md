
# HelloFromFlask

A full-stack microservice demo with a Python Flask backend and Vue.js frontend, orchestrated with Docker Compose.  
This project demonstrates manual and automated CI/CD as part of a DevOps portfolio.

---

## 🚀 Project Overview

- **Backend:** Python Flask API (`/api/hello`)
- **Frontend:** Vue.js app (fetches and displays backend message)
- **Orchestration:** Docker Compose
- **Manual & Automated CI/CD:** Documented and implemented

---

## 🏗️ Architecture

```
[ Vue.js (Nginx) ] <---> [ Flask API ]
        |                     |
     :8080                 :5000
```

![App Screenshot](public/images/your-screenshot.png)

---

## 🛠️ Getting Started

### Prerequisites

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/)

### Clone the Repo

```bash
git clone https://github.com/kqronos/HelloFromFlask.git
cd HelloFromFlask
```

### Manual CI/CD Workflow

1. **Build Docker images**
   ```bash
   docker-compose build
   ```

2. **Run tests**
   ```bash
   docker-compose run backend python -m unittest
   docker-compose run frontend npm run test
   ```

3. **Deploy (start services)**
   ```bash
   docker-compose up -d
   ```

4. **Update after code changes**
   ```bash
   docker-compose build
   docker-compose up -d
   ```

5. **Teardown**
   ```bash
   docker-compose down
   ```

---

## 🌐 Usage

- **Frontend:** [http://localhost:8080](http://localhost:8080)
- **Backend:** [http://localhost:5000/api/hello](http://localhost:5000/api/hello)

---

## 🧪 End-to-End Test

- Open the frontend in your browser.
- You should see the message from the Flask backend:  
  **"Hello from Flask!"**

---

## ⚙️ Technologies Used

- Python 3.11, Flask, Flask-CORS
- Vue.js, Nginx
- Docker, Docker Compose

---

## 📦 Project Structure

```
/backend      # Flask API
/frontend     # Vue.js app
/docker-compose.yml
/README.md
/public/images
```

---

## 📸 Screenshots

![Frontend Screenshot](public/images/frontend.png)
![Backend API Screenshot](public/images/backend.png)

---

## 🚦 CI/CD

- **Manual CI/CD:** See steps above.
- **Automated CI/CD:** [To be added in Step B]

---

## 📄 License

MIT

---

## Known Issues

None for now. ;)

# Future Improvments

It will be added styles and interactivity while the focus will be kept to monitor and update services along the way.