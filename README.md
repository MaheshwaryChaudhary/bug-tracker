# Bug Tracker

A full-stack Bug Tracking Web Application built by **Maheshwary Chaudhary** to help teams and developers **report, track, manage, and resolve software bugs efficiently**.

This tool is designed to be simple, responsive, and functional — combining a modern React frontend with Supabase backend services (database, authentication, real-time sync).

---

## 🧠 Project Overview

A bug tracking system allows developers, testers, and project managers to:

✅ Create new bug reports  
✅ Track open bugs and their status  
✅ Assign bugs to users  
✅ Update and resolve issues  
✅ View bug details and history  
✅ Search and filter bugs by priority, status, and type

This application utilizes **Supabase** for backend services (authentication, database, and realtime updates), enabling your app to store bug data and sync changes instantly.

---

## 📦 Features

### 🪲 Bug Reporting

- **Create a new bug report** with a title, description, severity, priority, and optionally attachments or screenshots.
- Bugs are stored with unique IDs, timestamps, and reporter metadata.

### 📋 Bug Management

- **Update bugs** to change status (Open, In Progress, Resolved, Closed).
- **Assign bugs** to specific users/team members.
- **Delete bugs** where appropriate.
- **View full details** of each bug, including comments, status history, and timestamps.

### 🔍 Search & Filters

- Filter bugs by **status**, **priority**, **type**, and **assignee**.
- Quick search by keywords in title or description.

### 🧑‍💻 Authentication

- Sign up and log in using Supabase Auth (email/password).
- Secure routes — only authenticated users can create or edit bugs.

### 📊 Real-Time Updates

- Via Supabase realtime features, updates from other users reflect instantly.
- See new bugs or status changes without page refresh.

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|------------|
| Frontend | React + TypeScript |
| UI Library | Tailwind CSS |
| Build Tool | Vite |
| Backend | Supabase (Database + Auth + Realtime) |
| Deployment | Optional netlify / vercel production host |

---

## 🚀 Quick Start

### 1. Clone Repo

```bash
git clone https://github.com/MaheshwaryChaudhary/bug-tracker.git
cd bug-tracker
2. Install Dependencies
npm install
3. Environment Variables
Create a .env file with your Supabase project credentials:

VITE_SUPABASE_URL=https://your-supabase-project.supabase.co
VITE_SUPABASE_ANON_KEY=your-public-anon-key
These variables connect your frontend to the Supabase backend services.

4. Run Dev Server
npm run dev
Open http://localhost:5173 in your browser.

🏗️ Folder Structure
src/
├─ components/       # React UI components
├─ pages/            # Route pages
├─ supabase/         # Supabase client + config
├─ styles/           # Tailwind & UI styles
├─ App.tsx           # App root
└─ main.tsx          # Vite entry
📌 How It Works
User signs up / logs in
Supabase Auth handles authentication and session management.

User creates a bug report
The app posts a new bug object to the Supabase database.

Bug appears in the list
Real-time sync updates the list immediately thanks to Supabase Realtime.

Users update bugs
Status, priority, assignments, and comments are edited directly and saved to the backend.

📁 Data Model (Example)
Field	Type	Description
id	UUID	Unique bug identifier
title	string	Short description of bug
description	text	Detailed bug info
status	string	Bug current state
priority	string	Priority level
created_at	timestamp	Time created
updated_at	timestamp	Time last updated
reporter	string	User who reported
assigne
