<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:6a11cb,100:2575fc&height=200&section=header&text=EventLens&fontSize=70&fontColor=ffffff&animation=fadeIn&fontAlignY=35&desc=A%20Poster-to-Event%20Hub%20for%20IEEE%20CS%20SRM%20IST%20Vadapalani&descAlignY=55&descSize=16" width="100%"/>

<img src="https://readme-typing-svg.demolab.com/?font=Fira+Code&size=22&pause=1500&color=6A11CB&center=true&vCenter=true&width=600&lines=Scan+a+Poster.+Extract+the+Event.+Done.;Discover.+Browse.+Manage.+Repeat." alt="Typing SVG" />

<br/><br/>

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![No Backend](https://img.shields.io/badge/Backend-None-lightgrey?style=for-the-badge)

</div>

<br/>

## Overview

**EventLens** is a single-page web app for discovering, browsing, and managing student-chapter events — seminars, workshops, hackathons, coding contests, and membership drives.

Its signature feature is a **"scan a poster"** upload flow that walks a flyer through a simulated OCR + NLP pipeline to auto-extract event details — name, date, time, venue, and category — before saving it into the event list.

<br/>

## Features

<table>
<tr>
<td width="50%" valign="top">

**Event Catalog**
Browse all chapter events in a responsive grid or list view.

**Search & Filter**
Full-text search plus category pills — Seminar, Workshop, Hackathon, Coding Challenge, Membership Drive.

**Date Range & Sorting**
Filter by date range, sort by date (asc/desc) or name.

</td>
<td width="50%" valign="top">

**Event Details Modal**
Click any event for a full detail view with description, metadata, and an extracted-data panel.

**Poster Upload Flow**
Drag-and-drop or select a JPEG/PNG/PDF poster; a simulated OCR/NLP pipeline extracts structured metadata with a confidence score, ready to review and save.

**Share**
Native Web Share API, with clipboard copy as a fallback.

**Status Badges**
Events are tagged Upcoming, Ongoing, or Past.

</td>
</tr>
</table>

<br/>

## Tech Stack

<div align="center">

| Layer        | Tech                                                          |
|--------------|------------------------------------------------------------------|
| Structure    | Plain HTML — no build step, no dependencies, no backend           |
| Styling      | Plain CSS + Google Fonts (DM Serif Display, DM Sans, JetBrains Mono) via CDN |
| Logic        | Vanilla JavaScript — all app state lives in memory                 |

</div>

<br/>

## Getting Started

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

<br/>

## Project Structure

```
EventLens/
└── index.html   # Entire app — markup, styles, and logic
```

<br/>

## Current Limitations

<details>
<summary><strong>This is a front-end prototype, not a production system — click for details</strong></summary>

<br/>

- **No real OCR/NLP backend.** The "poster scan" flow is a simulated demo — it plays a progress animation and returns metadata from a small rotating set of sample events rather than analyzing the uploaded file. Wiring up a real OCR engine (e.g. Tesseract) and an NLP classifier is a natural next step.
- **No persistence.** Events live in a JavaScript array in memory; refreshing the page resets everything to the seed data.
- **No authentication or backend storage**, so there's no real "submit to a shared repository" — it's local to your browser session.

</details>

<br/>

## Roadmap Ideas

- Hook up a real OCR service (Tesseract.js, Google Vision, or a backend API) for genuine poster parsing
- Add persistent storage (a database or even `localStorage`/a lightweight backend) so events survive a refresh
- Chapter-admin authentication for managing/approving submitted events
- Calendar export (ICS) and email/WhatsApp reminders for upcoming events

<br/>

## Contributing

Issues and pull requests are welcome. If you're extending the OCR pipeline or adding a backend, please open an issue first to discuss the approach.

<br/>

<div align="center">

Built for the **IEEE Computer Society Student Chapter, SRM IST Vadapalani**.

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2575fc,100:6a11cb&height=100&section=footer" width="100%"/>

</div>
