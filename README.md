# EventLens

**A poster-to-event hub for the IEEE Computer Society Student Chapter, SRM IST Vadapalani.**

EventLens is a single-page web app for discovering, browsing, and managing student-chapter events (seminars, workshops, hackathons, coding contests, and membership drives). Its signature feature is a "scan a poster" upload flow that walks a flyer through a simulated OCR + NLP pipeline to auto-extract event details — name, date, time, venue, and category — before saving it into the event list.

## ✨ Features

- **Event catalog** — browse all chapter events in a responsive grid or list view
- **Search & filter** — full-text search plus category pills (Seminar, Workshop, Hackathon, Coding Challenge, Membership Drive)
- **Date range & sorting** — filter by date range, sort by date (asc/desc) or name
- **Event details modal** — click any event for a full detail view with description, metadata, and extracted-data panel
- **Poster upload flow** — drag-and-drop or select a JPEG/PNG/PDF poster; a simulated OCR/NLP pipeline extracts structured event metadata with a confidence score, which you can review and save
- **Share** — share event details via the native Web Share API, with clipboard copy as a fallback
- **Status badges** — events are tagged Upcoming, Ongoing, or Past

## 🖥️ Tech Stack

- **Plain HTML, CSS, and vanilla JavaScript** — no build step, no dependencies, no backend
- Google Fonts (DM Serif Display, DM Sans, JetBrains Mono) loaded via CDN
- All app state lives in memory in a single `index.html` file

## 🚀 Getting Started

No installation required.

```bash
git clone https://github.com/SREEJITH-16/EventLens.git
cd EventLens
```

Then simply open `index.html` in your browser, or serve it locally:

```bash
# Python
python -m http.server 8000

# Node
npx serve .
```

Visit `http://localhost:8000` (or the port shown) and you're in.

## 📁 Project Structure

```
EventLens/
└── index.html   # Entire app — markup, styles, and logic
```

## ⚠️ Current Limitations

This is a front-end prototype, not a production system:

- **No real OCR/NLP backend.** The "poster scan" flow is a simulated demo — it plays a progress animation and returns metadata from a small rotating set of sample events rather than analyzing the uploaded file. Wiring up a real OCR engine (e.g. Tesseract) and an NLP classifier is a natural next step.
- **No persistence.** Events live in a JavaScript array in memory; refreshing the page resets everything to the seed data.
- **No authentication or backend storage**, so there's no real "submit to a shared repository" — it's local to your browser session.

## 🗺️ Roadmap Ideas

- Hook up a real OCR service (Tesseract.js, Google Vision, or a backend API) for genuine poster parsing
- Add persistent storage (a database or even `localStorage`/a lightweight backend) so events survive a refresh
- Chapter-admin authentication for managing/approving submitted events
- Calendar export (ICS) and email/WhatsApp reminders for upcoming events

## 🤝 Contributing

Issues and pull requests are welcome. If you're extending the OCR pipeline or adding a backend, please open an issue first to discuss the approach.



Built for the **IEEE Computer Society Student Chapter, SRM IST Vadapalani**.
