# Day 70 - Task Manager Backend (B43-FSD)

A robust Node.js and Express.js backend application integrated with MongoDB using Mongoose ODM. 

## 🚀 Features

- **Express Server**: Highly scalable backend architecture.
- **Database Connectivity**: Supports both MongoDB Local (Compass) and MongoDB Atlas (Cloud).
- **Data Validation**: Enforced schemas and status checks (`not-started`, `in-progress`, `completed`) using Mongoose.
- **Environment Safety**: Secure configuration management using `.env`.

---

## 🛠️ Tech Stack

- **Runtime**: Node.js
- **Framework**: Express.js (v5.x)
- **Database**: MongoDB
- **ODM**: Mongoose (v9.x)
- **Development Tool**: Nodemon

---

## 📂 Project Structure

```text
├── config/
│   └── dbconnection.config.js  # Database connection logic
├── models/
│   └── tasks.model.js          # Mongoose Task Schema and Model
├── .env                        # Environment variables (Local & Cloud)
├── .gitignore                  # Git untracked files configuration
├── main.js                     # Application entry point
├── package.json                # Dependencies and scripts
└── README.md                   # Project documentation
```

---

## ⚙️ Prerequisites

Before running this project, ensure you have the following installed:
- [Node.js](https://nodejs.org) (v16+ recommended)
- [MongoDB Community Server](https://mongodb.com) (for local DB)

---

## 🚀 Getting Started

Follow these steps to setup and run the project locally:

### 1. Clone the Repository
```bash
git clone https://github.com<your-username>/<your-repo-name>.git
cd <your-repo-name>
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Setup Environment Variables
Create a `.env` file in the root directory. Copy and update the placeholders with your actual configurations:
```env
port = <YOUR_SERVER_PORT>
dbport = mongodb://<YOUR_LOCAL_HOST>:<YOUR_LOCAL_DB_PORT>/<YOUR_LOCAL_DATABASE_NAME>

# Alternate Cloud DB Configuration (Atlas)
# atlasport = mongodb+srv://<YOUR_DB_USERNAME>:<YOUR_DB_PASSWORD>@<YOUR_CLUSTER_URL>/<YOUR_DATABASE_NAME>
```

### 4. Run the Application

**For Development (with Auto-Reload):**
```bash
npm run dev
```

**For Production:**
```bash
node main.js
```

---

## 📊 Database Schema (Tasks)

| Field | Type | Required | Validation / Rules |
| :--- | :--- | :--- | :--- |
| `title` | String | Yes | Unique task title |
| `description` | String | Yes | Detailed description of the task |
| `status` | String | Yes | Allowed values: `not-started`, `in-progress`, `completed` |
