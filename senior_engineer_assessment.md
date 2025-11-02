# Senior Software Engineer Practical Assessment

## Assessment Overview
**Time Limit:** 3-4 hours  
**Format:** Take-home assignment  
**Deliverables:** Working code + documentation

---

## The Challenge

### Scenario
You're leading the development of a new feature for "HealthTrack," a comprehensive health and wellness application. The product team wants to implement a "Health Insights Engine" that provides personalized health recommendations to users based on their activity data, vital signs, and health goals.

**Your Task:** Design and implement a scalable backend service that handles personalized health insights and recommendations.

---

## Technical Requirements

### Core Functionality
Build a RESTful API service that:

1. **Accepts health activity data**
   - Exercise sessions (type, duration, intensity)
   - Vital signs (heart rate, sleep hours, weight)
   - Nutrition logs (meals, water intake, calories)
   - Health goals (weight loss, better sleep, more exercise)

2. **Generates personalized health insights**
   - Based on user's health patterns and goals
   - Returns top 5 actionable recommendations
   - Considers user preferences and health history
   - Provides context and reasoning for each recommendation

3. **Handles scale considerations**
   - Service should be designed to handle 10K requests/minute
   - Discussion of caching strategy
   - Database design considerations
   - Privacy and security requirements for health data

### Technical Specifications
- **Language:** Your choice (Python, Node.js, Java, Go, etc.)
- **Database:** Your choice (can use in-memory if needed)
- **Framework:** Your choice
- **Testing:** Include unit tests for core logic

---

## What to Deliver

### 1. Working Code (2-2.5 hours)
- Functional API with at least 2 endpoints:
  - `POST /api/health-data` - Accept user health activity
  - `GET /api/insights/:userId` - Get personalized health recommendations
- Basic recommendation algorithm (rule-based or simple ML)
- Input validation and error handling
- HIPAA/privacy considerations in design

### 2. System Design Documentation (45 minutes)
Include:
- Architecture diagram showing key components
- Database schema design
- Scalability considerations and trade-offs
- Caching strategy
- How you would handle 10K requests/minute
- Security considerations

### 3. Code Documentation (30 minutes)
- README with setup instructions
- API documentation (endpoints, request/response formats)
- Explanation of your recommendation algorithm
- Known limitations and future improvements

### 4. Tests (30 minutes)
- Unit tests for core business logic
- At least 70% code coverage for critical paths
- Integration test for one happy path scenario

---

## Sample Data Format

### Input Health Data Example:
```json
{
  "userId": "user123",
  "dataType": "exercise",
  "activity": {
    "type": "running",
    "duration": 30,
    "intensity": "moderate",
    "caloriesBurned": 250
  },
  "timestamp": "2025-11-02T07:30:00Z",
  "metadata": {
    "heartRate": 145,
    "location": "outdoor"
  }
}
```

### Expected Insights Response:
```json
{
  "userId": "user123",
  "insights": [
    {
      "id": "insight_1",
      "category": "exercise",
      "recommendation": "Try adding 2 strength training sessions per week",
      "priority": "high",
      "reasoning": "Based on your consistent cardio routine, adding strength training will help with your weight loss goal",
      "confidence": 0.85
    },
    {
      "id": "insight_2",
      "category": "sleep",
      "recommendation": "Aim for 30 minutes earlier bedtime",
      "priority": "medium",
      "reasoning": "Your average sleep duration is 6.5 hours, below the recommended 7-9 hours",
      "confidence": 0.92
    }
  ],
  "generatedAt": "2025-11-02T10:35:00Z",
  "basedOnDays": 30
}
```

---

## Constraints & Assumptions

- You can seed initial health data for 2-3 sample users
- Focus on architecture and design over ML sophistication
- Simple rule-based recommendation logic is acceptable (e.g., "if sleep < 7 hours, recommend earlier bedtime")
- Consider basic health data privacy requirements
- Document any assumptions you make about health metrics or recommendations

---

## Submission Instructions

Please submit:
1. Git repository (GitHub, GitLab, or zip file)
2. README with setup instructions
3. System design documentation (PDF or Markdown)
4. Brief note on time spent and approach

**Send to:** [via Google Form provided (time constrained)]  
**Deadline:** [You must complete the assessment within 4 hours of starting it]

---
