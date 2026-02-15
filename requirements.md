# Requirements: AI-Powered Personalized Career Learning Assistant

## 1\. Overview

A web-based intelligent learning platform that analyzes a student’s current skills, identifies gaps based on career goals, and generates a personalized learning pathway. The system provides daily AI-guided lessons, automatically generated teaching videos, weekly assessments, and adaptive roadmap updates based on performance.

The goal of the system is to help students achieve career readiness through structured, personalized, and interactive AI-driven learning.

---

## 2\. User Stories

### 2.1 As a user, I want to create my profile

* I can select my branch (CSE, ECE, AI, etc.)
* I can select my year of study
* I can specify my career goal (Software Developer, Data Scientist, ML Engineer, etc.)
* I can enter known technologies
* I can upload my resume
* I can provide my GitHub link (optional)

---

### 2.2 As a user, I want AI to assess my skill level

* The AI chatbot asks technical questions based on my career goal
* Questions adapt based on my responses
* My answers are evaluated automatically
* I receive a skill score for each domain

---

### 2.3 As a user, I want a personalized roadmap

* The system generates a realistic multi-week learning plan
* The roadmap considers my current level and career goal
* The roadmap includes daily tasks and milestones
* The roadmap updates dynamically as I improve

---

### 2.4 As a user, I want AI to teach me daily

* I receive daily lessons with limited, focused content
* AI explains concepts interactively
* I can ask doubts during learning
* I receive a generated educational video for the lesson

---

### 2.5 As a user, I want progress tracking and motivation

* I see my daily learning streak
* I receive reminders to continue learning
* I see skill progress charts
* I receive achievements or badges

---

### 2.6 As a user, I want weekly evaluation

* I take weekly assessments
* My performance updates my skill scores
* My learning path adjusts based on results

---

## 3\. Acceptance Criteria

### 3.1 User Profiling

* **AC 3.1.1**: System stores user profile data successfully
* **AC 3.1.2**: Resume upload is processed using NLP
* **AC 3.1.3**: Skills are extracted from resume text
* **AC 3.1.4**: GitHub link is stored correctly

---

### 3.2 Skill Assessment

* **AC 3.2.1**: AI generates questions based on career goal
* **AC 3.2.2**: Questions adapt based on user answers
* **AC 3.2.3**: Answers are evaluated automatically
* **AC 3.2.4**: Skill scores are generated between 0–100

---

### 3.3 Skill Gap Analysis

* **AC 3.3.1**: System compares user skills with industry skill map
* **AC 3.3.2**: Missing skills are identified
* **AC 3.3.3**: Job readiness score is calculated
* **AC 3.3.4**: Gap percentage is displayed

---

### 3.4 Roadmap Generation

* **AC 3.4.1**: Roadmap contains weekly milestones
* **AC 3.4.2**: Roadmap contains daily learning tasks
* **AC 3.4.3**: Roadmap difficulty matches user level
* **AC 3.4.4**: Roadmap updates after assessments

---

### 3.5 Daily Learning Engine

* **AC 3.5.1**: AI delivers daily lessons
* **AC 3.5.2**: Lesson content is limited and focused
* **AC 3.5.3**: AI can answer user questions
* **AC 3.5.4**: Video is generated for each lesson

---

### 3.6 Weekly Assessment

* **AC 3.6.1**: Weekly test is generated automatically
* **AC 3.6.2**: Results update skill scores
* **AC 3.6.3**: Roadmap adjusts based on performance

---

### 3.7 Dashboard

* **AC 3.7.1**: Skill radar chart is displayed
* **AC 3.7.2**: Learning progress is displayed
* **AC 3.7.3**: Streak counter is visible
* **AC 3.7.4**: Job readiness score is shown

---

## 4\. Technical Requirements

### 4.1 Backend

* FastAPI / Flask server
* REST API endpoints
* Resume parsing using NLP libraries
* AI integration for chatbot and roadmap generation

---

### 4.2 Frontend

* React.js interface
* Dashboard with charts
* Chat interface for AI interaction
* Video player integration

---

### 4.3 AI Components

* NLP for resume parsing
* Skill similarity analysis using ML
* LLM for teaching and roadmap generation
* Automated video generation pipeline

---

## 5\. Non-Functional Requirements

### 5.1 Performance

* Profile processing < 5 seconds
* Roadmap generation < 10 seconds
* Video generation asynchronous

---

### 5.2 Usability

* Simple onboarding process
* Clear learning interface
* Mobile-responsive UI

---

### 5.3 Security

* JWT authentication
* Secure file upload
* Encrypted passwords

---

## 6\. Constraints

* Requires internet connection for AI services
* Video generation may take processing time
* Limited career domains initially supported

---

## 7\. Future Enhancements

* Voice-based AI tutor
* Mobile application
* Industry mentor integration
* Multi-language support
