# WebD-Selection-25-26-Task-1

# 🍽 The Main Course  
**Core Application Build – Up to 150 Points**  
This is the heart of the banquet. You'll build the robust backend engine and the delightful frontend experience that will leave users hungry for more.

---

## 🛠 Backend Banquet: Forging the API (90 Points)  
You are the source of all ingredients. You'll build a powerful API from scratch.

### **Database Alchemy (20 Points)**  
- Connect your server to a free **MongoDB Atlas** cluster.  
- The server should only start listening for requests **after** a successful connection to the database.

### **Crafting the Blueprints (20 Points)**  
Define your **Mongoose Schemas**:  
- **User**: `name`, `email`, `password`  
- **Question**: `title`, `url`, `difficulty` (enum: `'Easy'`, `'Medium'`, `'Hard'`)  
- **Category**: `title`, `questions` (array of Question references)

### **Summoning the Ingredients (15 Points)**  
- Write a **seeder script** to populate your database with data from:  
  [https://test-data-gules.vercel.app/data.json](https://test-data-gules.vercel.app/data.json)

### **The Grand API Gateway (35 Points)**  
Create the primary endpoint: 

It must support:  
- **Searching**: Filter results by question title (`?search=array`)  
- **Filtering**: Filter by difficulty (`?difficulty=Medium`)  
- **Pagination**: Control page & limit (`?page=2&limit=5`)

---

## 🎨 Frontend Feast: The Interactive Menu (60 Points)  
Design the elegant dining experience for your guests.

- **Serve from Your Kitchen**: Fetch all data from your backend API only.  
- **The Elegant Accordion**: Display categories & questions in collapsible format.  
- **Difficulty Flair**: Show a **color-coded tag** next to each question:  
  - Easy → Green  
  - Medium → Yellow  
  - Hard → Red  
- **Works Everywhere**: Fully responsive across all devices.

---

# 🍰 The Dessert & Liqueurs  
**Advanced Features & Bonus Points**

---

## 🍷 Full-Stack Confections (Backend + Frontend Integration)

### **The VIP Lounge: User Authentication (80 Points)**  
**Backend**:  
- Implement full auth flow:  
  - `POST /api/v1/auth/register`  
  - `POST /api/v1/auth/login`  
- Passwords hashed, JWT issued on login.

**Frontend**:  
- Beautiful Login/Register pages or modals.  
- Global user state.  
- Show username on login, update navbar, protect client-side routes.

---

### **The Personal Vault: Bookmarking & Progress (60 Points)**  
**Backend**:  
- Protected endpoints:  
  - `POST /api/v1/user/progress`  
  - `GET /api/v1/user/bookmarks`

**Frontend**:  
- Logged-in users can:
  - Check off completed questions  
  - Bookmark questions  
- `/dashboard` route:  
  - Progress bar  
  - List of bookmarked questions

---

## 🔮 Backend Elixirs (Server-Side Magic)

- **The Guardian** (30 Points): JWT verification middleware for all user-specific routes. Unauthenticated requests → `401 Unauthorized`.  
- **The Rate Limiter** (25 Points): Basic rate limiting on login/register to prevent brute-force attacks.  
- **The Sorter** (20 Points): Enhance `GET /api/v1/content` with sorting by name/difficulty (`?sortBy=difficulty_asc`).

---

## 🎭 Frontend Garnishes (UI/UX Delights)

- **The Alchemist's Toggle** (20 Points): Dark/Light mode with preference saved in `localStorage`.  
- **The Ghostly Search** (25 Points): Debounced search (e.g., 300ms delay).  
- **Fluidum Animate** (30 Points): Custom animations & transitions with **vanilla CSS only**.  
- **The Oracle's Voice** (60 Points): Integrate **Web Speech API** for voice commands like “Open Arrays” or “Next Question”.

---

## 🎯 Rules of the Banquet

1. **Sign Your Masterpiece**:  
   - Include your **Name** and **Enrollment Number** in `README.md`.

2. **Frontend Purity**:  
   - React and frameworks can be used.  

3. **Original Recipes Only**:  
   - Plagiarism = ❌ disqualification.  
   - Your code will be checked.

4. **Learn, Don’t Lift**:  
   - Learning from resources is fine.  
   - Don’t copy large chunks from AI or other sources.

---
