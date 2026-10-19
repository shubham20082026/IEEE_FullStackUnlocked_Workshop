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

Here’s a clean, ready-to-copy version **starting from Section 4** onwards (in proper Markdown format):

```markdown
### 4. Backend Development with Flask

I created my first server using a minimal Flask application:

```python
from flask import Flask

app = Flask(__name__)

@app.route("/")
def home():
    return "API is running"

app.run(port=5000)
```

- Learned how to spin up a local server (`localhost:5000`).
- Understood the concept of routes and returning responses.
- Built my first real API endpoint: `GET /api/events` that returns a list of events in JSON format.

### 5. APIs – How Frontend and Backend Talk

An **API (Application Programming Interface)** is the bridge between frontend and backend.

I understood it with a simple analogy:  
> Just like a waiter takes your order to the kitchen and brings back your food, the API carries requests between the frontend and the backend.

Key concepts I learned:
- **Request → Response** cycle
- `GET` = “Give me data”
- JSON as the universal data format the frontend can easily read and display
- Example response:

```json
[
  {
    "title": "AI Workshop",
    "club": "IEEE CS"
  }
]
```

I created a `GET /api/events` endpoint that returns sample event data and tested it directly in the browser.

### 6. Connecting the Pieces

I learned how to:
- Make the frontend call the backend API
- Send and receive JSON data
- Dynamically update the UI based on the response
- Solve the “data disappears on refresh” problem by introducing a proper backend + storage layer

---

## Project Structure (Typical)

```
Full-Stack-Unlocked/
├── frontend/
│   ├── index.html          # Structure of the Event Tracker
│   ├── style.css           # All styling
│   └── script.js           # Form handling + dynamic rendering
├── backend/
│   ├── app.py              # Flask server + API routes
│   └── ...                 # Database helpers (if used)
├── README.md
└── .gitignore
```

---

## How to Run the Project

### Frontend only
1. Open `index.html` in a browser (or use Live Server in VS Code).

### Full Stack (Frontend + Backend)
1. Navigate to the backend folder.
2. Install Flask if needed:
   ```bash
   pip install flask
   ```
3. Run the server:
   ```bash
   python app.py
   ```
4. Open the frontend and make sure API calls point to `http://localhost:5000`.

---

## Key Milestones I Completed

- [x] Built a clean HTML structure for the event creation form
- [x] Styled the form and event cards with CSS
- [x] Added JavaScript to detect clicks, read form data, and render events dynamically
- [x] Initialised a Git repository and pushed the frontend to GitHub
- [x] Created a minimal Flask server
- [x] Built a `GET /api/events` endpoint that returns JSON
- [x] Understood the full request–response cycle between frontend and backend

---

## What This Workshop Taught Me Beyond Code

- How to break a real application into layers and build one piece at a time
- The importance of version control from day one
- Why APIs exist and how they enable modern web applications
- How to go from a static HTML page to a dynamic, data-driven application
- Confidence that I can build a complete full-stack project from scratch

---

## Workshop Details

- **Organised by**: IEEE Computer Society – MIT Bengaluru CS Chapter
- **Workshop Name**: Full Stack Unlocked
- **Goal**: Build your first full-stack app from scratch
- **Reference Repo**: [https://github.com/nirvika28/Full-Stack-Unlocked-IEEE-CS](https://github.com/nirvika28/Full-Stack-Unlocked-IEEE-CS)

---

## Next Steps / Possible Improvements

- Add POST endpoint to actually create events from the form
- Connect a real database (SQLite / PostgreSQL)
- Add edit and delete functionality for events
- Improve UI/UX (loading states, form validation, better card design)
- Deploy the full application (frontend + backend)

---

**Built with curiosity during the Full Stack Unlocked workshop.**  
One app. Built by me. From scratch.
```
