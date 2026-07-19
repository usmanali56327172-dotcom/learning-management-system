# Learning Management System (Full-Stack Web Application)

A production-grade, console-free web application simulating a Udemy/Coursera-style Learning Management System, developed as a full-stack engineering portfolio project.
The system demonstrates practical use of a layered backend architecture, a relational database, real-time communication, and a modern component-based frontend to manage courses, users, payments, and progress tracking.

---

## Features

### Authentication & Roles
- Sign up, login, logout with JWT (access token + rotating refresh token)
- Forgot/reset password flow
- Role-based access: Student, Instructor, Admin

### Course Management
- Instructors create, edit, and delete courses
- Curriculum builder: sections → lessons (video, article, quiz, assignment)
- Draft → Pending Review → Published workflow with admin approval

### Video Lessons & Learning Player
- Structured video/article playback with a persistent curriculum sidebar
- Lesson preview for non-enrolled visitors

### Quizzes
- Instructor-authored multiple-choice quizzes
- Auto-graded attempts with pass/fail thresholds

### Assignments
- Instructor-authored briefs with submission + grading workflow
- Score and feedback returned to the student

### Certificates
- Auto-issued on 100% course completion
- Unique serial number with a public verification endpoint

### Progress Tracking
- Per-lesson completion and watch-time
- Rolled up into an enrollment-level completion percentage

### Bookmarks & Wishlist
- Timestamped bookmarks on any lesson
- Save courses to a wishlist for later

### Reviews & Ratings
- One review per enrolled student per course
- Course rating aggregates recompute automatically

### Course Search
- Filter by category, level, and price
- Sort by newest, popularity, rating, or price

### Payments
- Stripe Checkout integration for paid courses
- Webhook-driven, idempotent enrollment fulfillment

### Notifications
- Persisted notification history
- Live delivery over Socket.IO

### Messaging
- Direct conversations between students and instructors
- Real-time message delivery over Socket.IO

### Analytics & Reports
- Instructor dashboard: revenue, enrollments, ratings, trends
- Admin dashboard: platform-wide users, courses, revenue

### Admin Management
- User search, suspend/reactivate, role change
- Course moderation queue (approve/reject with reason)
- Immutable admin audit log

### Responsive Design & Dark Mode
- Mobile-first layout
- Persisted dark/light theme preference

---

## Tech Stack Used

| Layer | Technology | Purpose |
|---|---|---|
| Backend | Node.js, Express, TypeScript | REST API server |
| Database | PostgreSQL + Prisma ORM | Relational data storage, type-safe queries |
| Auth | JWT + bcrypt | Stateless authentication, password hashing |
| Real-time | Socket.IO | Live notifications and messaging |
| Payments | Stripe Checkout + Webhooks | Course payments |
| Frontend | React 18, TypeScript, Vite | User interface |
| Styling | Tailwind CSS | Responsive, themeable UI |
| Data Fetching | TanStack Query | Server state, caching |
| State Management | Zustand | Auth/theme client state |
| Testing | Jest + Supertest | API integration tests |
| Containers | Docker + docker-compose | Local environment, deployment |

---
