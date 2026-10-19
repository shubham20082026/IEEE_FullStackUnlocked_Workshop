# IEEE FULL STACK UNLOCKED WORKSHOP
# Full Stack Unlocked – College Event Tracker

**A hands-on workshop by IEEE Computer Society (MIT BLR CS Chapter)**  
**Build your first full-stack application from scratch.**

This repository contains the complete College Event Tracker application I built during the **Full Stack Unlocked** workshop. Starting from a blank page, I progressively created a working full-stack web app that lets users create and view college events.

---

## What I Built

I built a **College Event Tracker** — a simple but complete full-stack web application where users can:

- Create new events with the following fields:
  - Event Title
  - Club / Organiser
  - Date
  - Venue
  - Description
- Click a **Create Event** button to submit the form
- See the newly created event appear instantly as a card on the page
- Persist events so they don’t disappear on page refresh (once the backend + database layer is connected)

### App Flow
1. User fills out the “Create an Event” form on the frontend.
2. JavaScript reads the form values when the button is clicked.
3. The frontend sends a request to the backend API.
4. The backend processes the request and stores the data.
5. The frontend receives the response (JSON) and dynamically renders the event card.

By the end of the workshop I had a working frontend + backend connected through an API, with Git version control throughout the process.

---

## Tech Stack

| Layer       | Technologies                          | Purpose                                      |
|-------------|---------------------------------------|----------------------------------------------|
| Frontend    | HTML, CSS, JavaScript                 | Structure, styling, and interactivity        |
| Backend     | Python + Flask                        | Server, business logic, and API endpoints    |
| Database    | SQLite (via Flask)                    | Persistent storage of events                 |
| Version Control | Git + GitHub                       | Track changes and share the project          |
| Communication | REST API + JSON                    | Frontend ↔ Backend data exchange             |

---

## What I Learned

### 1. The Three Layers of a Full-Stack Application
Every web application is built on three distinct layers:

- **Frontend** – What the user sees and interacts with (runs in the browser)
- **Backend** – The logic and processing layer (handles requests, applies rules, talks to the database)
- **Database** – Permanent storage so data survives page refreshes

**Frontend + Backend + Database = Full Stack**

I learned how these layers communicate and why each one is necessary.

### 2. Frontend Fundamentals

#### HTML → Structure
- HTML defines the skeleton of the page using elements and tags.
- I created a form with fields for Event Title, Club, Date, Venue, and Description, plus a “Create Event” button and a section to display events.
- Learned about nested elements, hierarchy, and how the browser interprets HTML.

#### CSS → Style
- Transformed a plain, unstyled form into a clean, modern-looking interface.
- Practiced controlling:
  - Colours
  - Fonts
  - Spacing and padding
  - Borders and border-radius
  - Layout (including Flexbox concepts)
  - Hover states on buttons
- Understood the difference between raw HTML and a polished UI.

#### JavaScript → Behaviour
- Without JavaScript, clicking a button does nothing.
- I learned the core interaction cycle:
  1. User clicks the button → event listener fires
  2. JavaScript detects the click
  3. Reads values from the form inputs (`getElementById` / `querySelector`)
  4. Dynamically creates and inserts a new event card into the page (no page reload)

This was the first time the page felt *alive*.

### 3. Version Control with Git & GitHub
I learned why version control is essential and practiced the basic workflow:

```bash
git init                          # Initialise a new repository
git add .                         # Stage all changes
git commit -m "Created event tracker frontend"
git push -u origin master         # Push to GitHub
