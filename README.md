<div align="center">

# 🌍 Y A T R A W A Y
### *GlobeTrotter Multi-City Travel Planner & Smart AI Itinerary Engine*

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Cinzel&weight=700&size=26&pause=1000&color=C9963A&center=true&vCenter=true&width=650&lines=Curate+Multi-City+Adventures;Gemini+AI+Smart+Route+Optimizer;Automatic+Budget+Calculator;Discover+Your+Travel+DNA+Persona;Public+Trip+Sharing+%26+Community)](https://git.io/typing-svg)

<p align="center">
  <img src="https://img.shields.io/badge/React_18-Vite_5.4-61DAFB?style=for-the-badge&logo=react&logoColor=black" alt="React" />
  <img src="https://img.shields.io/badge/Node.js-Express_API-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" alt="Node" />
  <img src="https://img.shields.io/badge/Google_Gemini-2.5_Flash_AI-4285F4?style=for-the-badge&logo=google&logoColor=white" alt="Gemini AI" />
  <img src="https://img.shields.io/badge/Supabase-Auth_%26_Database-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white" alt="Supabase" />
  <img src="https://img.shields.io/badge/Framer_Motion-Smooth_Physics-0055FF?style=for-the-badge&logo=framer&logoColor=white" alt="Framer Motion" />
</p>

---

[🚀 Explore Live Demo](http://localhost:5173/) • [✨ Features](#-core-features) • [🧠 AI Optimizer](#-gemini-ai-smart-trip-optimizer) • [🏗️ Architecture](#-system-architecture--data-schema) • [📡 API Reference](#-api-endpoints) • [⚙️ Installation](#-getting-started)

---

</div>

## 📌 Executive Summary

Planning a multi-city vacation requires juggling disparate booking portals, calculating fluctuating expenses, structuring day-wise activities, and keeping track of complex transit routes.

**YatraWay (GlobeTrotter)** is an elite, editorial travel planning platform that unites destination exploration, multi-city route orchestration, automatic budget estimation, interactive calendar timelines, and Gemini-powered smart trip optimization into a single unified platform.

```
                    ┌──────────────┐
                    │ LOGIN/SIGNUP │
                    └──────┬───────┘
                           ↓
                    ┌──────────────┐
                    │  DASHBOARD   │
                    └──────┬───────┘
                           ↓
                  ┌─────────────────┐
                  │  CREATE TRIP    │
                  └────────┬────────┘
                           ↓
                ┌────────────────────┐
                │   ADD DESTINATIONS │
                └──────────┬─────────┘
                           ↓
                ┌────────────────────┐
                │  ADD ACTIVITIES    │
                └──────────┬─────────┘
                           ↓
                ┌────────────────────┐
                │ BUILD ITINERARY    │
                └──────────┬─────────┘
                           ↓
                ┌────────────────────┐
                │ AUTO CALCULATE $$$ │
                └──────────┬─────────┘
                           ↓
               ┌─────────────────────┐
               │ CALENDAR / TIMELINE │
               └──────────┬──────────┘
                          ↓
               ┌─────────────────────┐
               │ SHARE / COMMUNITY   │
               └─────────────────────┘
```

---

## ✨ Core Features

### 1. 🤖 Gemini AI Smart Trip Optimizer
- **Intelligent Multi-City Sequencing**: Reorders stop sequences to minimize inter-city transit times by up to 4.2 hours.
- **Geographic Landmark Clustering**: Clusters morning and afternoon monuments to eliminate backtracking.
- **Automated Pacing & Savings**: Tailors daily density to your selected pace (Slow, Active, Luxury) with bundled activity cost savings.

### 2. 🗺️ Interactive Multi-City Itinerary Builder
- **Dynamic City Stops**: Add and reorder stops (*e.g. Paris 4d → Rome 5d → Barcelona 5d*).
- **Day-Wise Activity Blocks**: Timed slots (`10:00 AM`, `02:00 PM`, `06:30 PM`), category tags (*Culture, Food, Adventure, Sightseeing, Shopping*), and itemized costs in ₹ INR.
- **Full Activity CRUD**: Add custom activities or remove stops with live automatic recalculation.

### 3. 💰 Automatic Live Budget Calculator
- **Real-Time Cost Aggregation**: Instant categorization across **🏨 Hotels**, **✈️ Transport**, **🎯 Activities**, and **🍽️ Dining**.
- **Daily Average Cost Metric**: Computes accurate `₹/day` across multi-city durations.
- **Budget Variance & Alerts**: Highlights savings or warns if planned expenses exceed target budget.

### 4. 🗓️ Interactive Calendar & Timeline Visualization
- Monthly calendar grid view mapping multi-city stops.
- Click any date to view scheduled morning-to-night activity timelines.

### 5. 🧭 Travel Style & Persona Discovery Engine
- 4-dimensional assessment evaluating Landscape, Pace, Investment Tier, and Companionship.
- Identifies your **Travel DNA Archetype** (*The High-Altitude Alpine Nomad, The Coastal Sanctuary Seeker, The Royal Heritage Connoisseur, The Holistic Ayurveda Wanderer*).
- Directly exports matching destinations into `/trips` with 1 click.

### 6. 🔗 Public Trip Sharing & Community Copy
- Generates unique public URLs (`/trips?share=:id`).
- **`📋 Copy This Trip to My Journeys`**: Clones and imports full multi-city itineraries into personal accounts with 1 click.

---

## 🏗️ System Architecture & Data Schema

```
USER
 │
 │ 1:N
 ↓
TRIP
 │
 ├──────────────────────────────┐
 ↓                              ↓
TRIP_STOP (Cities & Dates)     EXPENSE (Hotels, Flights, Food)
 │
 │ N:1
 ↓
CITY
 │
 │ 1:N
 ↓
ACTIVITY (Culture, Sightseeing, Dining)
 │
 ↓
ITINERARY_ITEM (Day #, Time Slots, Cost in ₹)
```

---

## 📡 API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| `POST` | `/api/gemini/optimize-itinerary` | AI smart multi-city optimizer with day-wise budget calculations |
| `POST` | `/api/gemini/generate-destinations` | Personalized solo & women-safe destination curation |
| `GET` | `/api/trips` | Fetch all user journeys and itineraries |
| `POST` | `/api/trips` | Create a new multi-city journey |
| `PUT` | `/api/trips/:id` | Update itinerary stops, activities, and expenses |
| `DELETE` | `/api/trips/:id` | Delete journey |
| `GET` | `/api/bookings` | Fetch confirmed flight, hotel, and logistics vouchers |
| `POST` | `/api/bookings` | Create confirmed logistics reservation |
| `GET` | `/api/emergency/sos` | Instant 24/7 emergency response & local authority directory |

---

## ⚙️ Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/dhyeyptl10/YatraWay.git
cd YatraWay
```

### 2. Configure Backend
```bash
cd backend
npm install
npm run dev
```
*Create a `.env` file in `backend/`:*
```env
PORT=5000
GEMINI_API_KEY=your_google_gemini_api_key
SUPABASE_URL=your_supabase_url
SUPABASE_KEY=your_supabase_service_key
```

### 3. Configure Frontend
```bash
cd ../frontend
npm install
npm run dev
```
*Create a `.env` file in `frontend/`:*
```env
VITE_API_URL=http://localhost:5000/api
VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
```

---

<div align="center">
  <sub>Built with ❤️ for passionate travelers worldwide. GlobeTrotter Hackathon Edition.</sub>
</div>


