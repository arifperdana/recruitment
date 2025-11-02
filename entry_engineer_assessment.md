# Entry-Level Software Engineer Practical Assessment

## Assessment Overview
**Time Limit:** 2-3 hours  
**Format:** Take-home assignment  
**Deliverables:** Working code + brief documentation

---

## The Challenge

### Scenario
You're building a feature for "HealthTrack," a health and wellness application. Users need a way to log and track their daily water intake to stay hydrated.

**Your Task:** Build a basic REST API for a water intake tracking system.

---

## Technical Requirements

### Core Functionality
Build an API that supports:

1. **Log water intake**
   - Amount in milliliters (required)
   - Timestamp (auto-generated or provided)
   - Optional note (e.g., "morning coffee", "post-workout")

2. **Get daily water intake**
   - Total water consumed today
   - List of all water logs for the day
   - Progress toward daily goal (e.g., 2000ml)

3. **Set/update daily goal**
   - User can set their daily water intake target
   - Default: 2000ml (approximately 8 glasses)

4. **Get water intake history**
   - View logs for a specific date
   - Optional: Get weekly summary

### Technical Specifications
- **Language:** Your choice (Python, JavaScript/Node.js, Java, etc.)
- **Storage:** In-memory is fine (array, dictionary, etc.)
- **Framework:** Use any framework you're comfortable with
- **Testing:** At least 2-3 basic tests

---

## What to Deliver

### 1. Working API (1.5-2 hours)
Implement these endpoints:
- `POST /water-logs` - Log water intake
- `GET /water-logs/today` - Get today's water intake summary
- `GET /water-logs?date=YYYY-MM-DD` - Get logs for specific date
- `POST /daily-goal` - Set daily water intake goal
- `GET /daily-goal` - Get current daily goal

### 2. Basic Documentation (30 minutes)
A README file with:
- How to run your application
- List of API endpoints with examples
- Any dependencies needed

### 3. Tests (30 minutes)
Write at least 2-3 tests, such as:
- Logging water intake successfully
- Getting today's total water intake
- Calculating progress toward daily goal

---

## Evaluation Criteria

**Functionality (40%)**
- Does the API work as expected?
- Are all required endpoints implemented?
- Proper HTTP methods and status codes

**Code Quality (30%)**
- Clean and readable code
- Proper variable naming
- Basic error handling

**Documentation (20%)**
- Clear setup instructions
- API usage examples
- Code comments where needed

**Testing (10%)**
- Basic test coverage
- Tests actually run and pass

---

## Example API Usage

### Log Water Intake:
```bash
POST /water-logs
Content-Type: application/json

{
  "amount": 250,
  "note": "Morning glass of water",
  "timestamp": "2025-11-02T08:00:00Z"
}
```

**Response:**
```json
{
  "id": "1",
  "amount": 250,
  "note": "Morning glass of water",
  "timestamp": "2025-11-02T08:00:00Z"
}
```

### Get Today's Summary:
```bash
GET /water-logs/today
```

**Response:**
```json
{
  "date": "2025-11-02",
  "totalAmount": 1500,
  "dailyGoal": 2000,
  "progressPercentage": 75,
  "logs": [
    {
      "id": "1",
      "amount": 250,
      "timestamp": "2025-11-02T08:00:00Z"
    },
    {
      "id": "2",
      "amount": 500,
      "timestamp": "2025-11-02T12:30:00Z"
    },
    {
      "id": "3",
      "amount": 750,
      "timestamp": "2025-11-02T18:00:00Z"
    }
  ]
}
```

---

## What You Don't Need

- User authentication
- Database setup (in-memory storage is fine)
- Frontend/UI
- Advanced features like search or sorting
- Deployment or hosting

---

## Submission Instructions

Please submit:
1. Your code (GitHub repo or zip file)
2. README with setup instructions
3. Brief note on what you found challenging

**Send to:** [via Google Form provided (time constrained)]  
**Deadline:** [You must complete the assessment within 3 hours of starting it]

---
