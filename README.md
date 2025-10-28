# Job-Scheduling-Assignment
# 🧩 Digantara Job Scheduler Microservice

This service allows you to **create, list, and fetch scheduled jobs** (e.g., email notifications, data crunching tasks).

## 🚀 Features
- Job CRUD APIs (GET all, GET by ID, POST new job)
- MongoDB for persistent job info
- Dummy job execution using `node-cron`
- Centralized error handling
- Scalable modular structure

## 🧱 API Endpoints
| Method | Endpoint | Description |
|---------|-----------|-------------|
| GET | `/api/job` | List all jobs |
| GET | `/api/job/:id` | Get job by ID |
| POST | `/api/job` | Create & schedule a new job |

**Example Request (POST /api/job)**
```json
{
  "jobName": "Email Notification",
  "description": "Send reminder emails",
  "scheduleInterval": "*/5 * * * *",
  "config": {
    "recipient": "user@example.com"
  }
}