# Design: AI-Powered Personalized Career Learning Assistant

## 1\. System Architecture

### 1.1 High-Level Architecture

```
┌──────────────────────┐        HTTPS        ┌────────────────────────┐
│                      │ ◄──────────────────► │                        │
│     React Client     │     REST APIs        │     Backend Server     │
│                      │                      │   (FastAPI / Flask)    │
└──────────┬───────────┘                      └──────────┬─────────────┘
           │                                              │
           │                                              │
     ┌─────▼─────┐                               ┌────────▼────────┐
     │ Dashboard │                               │   AI Services    │
     │  Charts   │                               │ (LLM + NLP + ML) │
     └───────────┘                               └────────┬────────┘
                                                           │
                                               ┌───────────▼──────────┐
                                               │ Database + Storage    │
                                               │ (PostgreSQL / Cloud)  │
                                               └───────────────────────┘
```

The system is a web-based intelligent learning platform that evaluates user skills, identifies gaps, generates personalized learning roadmaps, delivers AI-taught lessons, and produces educational videos automatically.

---

### 1.2 Component Breakdown

#### Backend Components

1. **Authentication Module**

   * User registration and login
   * JWT-based authentication
   * Session management

2. **User Profiling Module**

   * Profile data storage
   * Resume upload handling
   * Resume parsing using NLP
   * GitHub link processing

3. **Skill Assessment Engine**

   * AI-based question generation
   * Adaptive difficulty logic
   * Answer evaluation using AI
   * Skill score calculation

4. **Skill Gap Analyzer**

   * Industry skill mapping
   * Gap computation
   * Job readiness scoring

5. **Roadmap Generator**

   * Generates a personalized career roadmap based on the user’s current skill level and target goals.
   * Weekly milestone planning
   * Daily task generation

6. **Adaptive Learning Engine**

   * Daily lesson delivery
   * Interactive AI teaching
   * Difficulty adjustment
   * Learning progress tracking

7. **Video Generation Service**

   * Lesson script generation
   * Slide creation
   * Text-to-speech narration
   * Video rendering

8. **Assessment Module**

   * Weekly test generation
   * Performance evaluation
   * Skill score updates

9. **Analytics \& Streak Engine**

   * Streak tracking
   * Progress monitoring
   * Dashboard statistics

---

#### Frontend Components

1. Authentication Pages
2. Profile Setup Page
3. AI Chat Interface
4. Dashboard
5. Learning Module
6. Assessment Module
7. Video Player Component

---

## 2\. Data Models

### 2.1 User Model

```json
{
  "userId": "",
  "name": "",
  "email": "",
  "branch": "",
  "year": "",
  "careerGoal": "",
  "skills": \[],
  "resumeUrl": "",
  "githubLink": ""
}
```

---

### 2.2 Skill Score Model

```json
{
  "skill": "DSA",
  "score": 75
}
```

---

### 2.3 Roadmap Model

```json
{
  "week": 1,
  "topics": \[],
  "tasks": \[],
  "difficulty": "Beginner"
}
```

---

### 2.4 Lesson Model

```json
{
  "day": 1,
  "topic": "",
  "content": "",
  "videoUrl": ""
}
```

---

## 3\. Algorithm Design

### 3.1 Skill Assessment Algorithm

**Steps:**

1. Identify required skills based on career goal.
2. Generate adaptive questions using AI.
3. Evaluate user responses using scoring logic.
4. Assign skill score between 0–100.

---

### 3.2 Skill Gap Analysis Algorithm

**Formula:**

Skill Gap = Required Skill Level − Current Skill Level

**Techniques:**

* Cosine similarity
* Weighted scoring system
* Rule-based evaluation

---

### 3.3 Roadmap Generation Algorithm

**Steps:**

1. Input user profile and skill scores.
2. Determine learning duration and pace.
3. Generate weekly milestones.
4. Break milestones into daily tasks.
5. Adjust difficulty dynamically.

---

### 3.4 Adaptive Learning Algorithm

After each assessment:

1. Update skill scores.
2. Recalculate skill gaps.
3. Modify roadmap difficulty.
4. Recommend next learning steps.

---

### 3.5 Video Generation Pipeline

**Steps:**

1. Generate lesson content using AI.
2. Convert content into teaching script.
3. Generate slides automatically.
4. Create narration using text-to-speech.
5. Render final video output.

---

## 4\. API Design

### Endpoints

POST /register
POST /login
POST /profile
POST /assessment/start
POST /assessment/submit
GET /roadmap
GET /lesson/today
POST /lesson/complete
GET /weekly-test
POST /weekly-submit
GET /dashboard

---

## 5\. Frontend Design

### Component Hierarchy

```
App
├── Authentication
├── Profile Setup
├── Dashboard
├── AI Chat Interface
├── Learning Module
└── Assessment Module
```

---

## 6\. Deployment Architecture

Frontend → Vercel / Netlify
Backend → Cloud Server (AWS / GCP / Azure)
Database → PostgreSQL / MongoDB
Storage → Cloud Storage (Videos \& Resumes)

---

## 7\. Testing Strategy

### Unit Testing

* Skill scoring logic
* Gap calculation
* Roadmap generation

### Integration Testing

* Profile → Assessment → Roadmap flow

### End-to-End Testing

* Complete learning cycle validation

---

## 8\. Performance Considerations

* Asynchronous video generation pipeline
* Efficient database indexing
* Caching frequently accessed data

---

## 9\. Security Considerations

* JWT authentication
* Secure password hashing
* Input validation
* Secure file upload handling

---

## 10\. Correctness Properties

### Property 10.1 Skill Scores Validity

* All skill scores must remain within 0–100 range.

### Property 10.2 Roadmap Consistency

* Generated roadmap must align with career goal.

### Property 10.3 Adaptive Updates

* Roadmap updates after assessments must reflect new skill scores.

### Property 10.4 Lesson Continuity

* Daily lessons must follow logical sequence progression.

---

## 11\. Future Enhancements

* Voice-based AI tutor
* Reinforcement learning personalization
* Mentor integration
* Mobile application

---

## 12\. Conclusion

The system integrates AI-based assessment, adaptive learning, and automated video generation to provide a personalized career learning experience. The architecture supports scalability, modularity, and continuous improvement based on user progress.

---

**End of Design Document**


