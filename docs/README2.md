<a name="readme-top"></a>

<h1 align="center">meta-bookclub</h1>
<h4 align="center"><ins><strong><em>* a personalized book and poem recommendation system * </em></strong></ins></h4>

<p align="center">
  <a href="https://www.linkedin.com/in/lyndsey791/">LinkedIn</a> |
  <a href="https://github.com/lyndskg/">GitHub</a> |
  <a href="#contact">Contact</a>
</p>

---

## Contents
- [Overview](#Overview)
  - [Objectives](#Objectives)
  - [Current Notes / Issues](#Current)
- [Key Features](#KeyFeatures)
- [Tech Stack](#TechStack)
  - [Desktop Application](#DesktopApp)
  - [Web Application](#WebApp)
  - [APIs / External Dependencies](#APIs)
- [Architecture](#Architecture)
  - [Data Models](#DataModels)
- [Basic Workflow](#BasicWorkflow)
- [I/O Specifications](#BasicIO)
- [Implementation Guide](#Implementation)
- [Roadmap](#Roadmap)
  - [To‑Do List](#ToDo)
  - [Estimated Timeline](#Timeline)
- [Installation](#Installation)
  - [Usage](#Usage)
- [Contributions](#Contribute)
- [Conclusion](#Conclusion)
- [Contact](#contact)

---

<a name="Overview"></a>
## Project Overview

**meta-bookclub** is an AI‑powered recommendation system that generates personalized reading suggestions across books, poems, essays, and long‑form writing. It analyzes user reading history (Goodreads, Kindle, manual input), metadata, and taste patterns to build a dynamic “taste vector” and produce recommendations that reflect the user’s actual literary identity.

The system supports both **web** and **desktop** implementations, with optional ML‑powered semantic embeddings, metadata enrichment, and user‑controlled preference tuning.

---

<a name="Objectives"></a>
## Objectives
1. Build a personalized recommendation engine that prioritizes individual taste over popularity.
2. Support books, poems, essays, and other literary formats.
3. Integrate with Goodreads, Kindle, OpenLibrary, and other metadata sources.
4. Provide a UI for browsing recommendations, editing preferences, and rating items.
5. Implement ML models for semantic similarity, clustering, and taste profiling.
6. Allow manual tagging and metadata editing to refine recommendations.
7. Support both web and desktop versions for flexibility.

---

<a name="Current"></a>
## Current Notes / Issues
- Goodreads API is deprecated; alternatives required.
- Kindle data extraction requires user‑side export.
- No finalized embedding pipeline.
- No UI implemented yet.
- Need a unified metadata schema for books + poems.

---

<a name="KeyFeatures"></a>
## Key Features
- ML‑driven personalized recommendations.
- Semantic embeddings for books and poems.
- Integration with Goodreads, Kindle, OpenLibrary, Google Books.
- Taste vector modeling and user preference weighting.
- Manual tagging and metadata editing.
- Reading history ingestion and analysis.
- Optional desktop app for offline use.
- Exportable reading lists and collections.

---

<a name="TechStack"></a>
## Technologies & Programming Languages

### Core Languages
- **Python** — backend, ML pipeline, data ingestion.
- **JavaScript / TypeScript** — frontend (React), desktop wrapper (Electron).
- **SQL** — metadata storage (SQLite or PostgreSQL).

---

<a name="DesktopApp"></a>
### Desktop Application (Optional)
**Version 1**
- **Frontend:** Electron.js  
- **Backend:** Python (FastAPI or Flask)  
- **ML:** PyTorch or TensorFlow  
- **Database:** SQLite  
- **Libraries:** SentenceTransformers, spaCy, scikit‑learn  

**Version 2**
- **Frontend:** Flutter or React Native Desktop  
- **Backend:** .NET or Python  
- **Metadata APIs:** Google Books, OpenLibrary  

---

<a name="WebApp"></a>
### Web Application
**Version 1**
- **Frontend:** React or Svelte  
- **Backend:** FastAPI or Flask  
- **ML:** Python‑based embedding pipeline  
- **Database:** PostgreSQL or SQLite  

**Version 2**
- **Frontend:** Angular or Vue  
- **Backend:** Django or Ruby on Rails  
- **Client‑side ML:** TensorFlow.js (optional)

---

<a name="APIs"></a>
### APIs / External Dependencies
- Google Books API  
- OpenLibrary API  
- Optional: Goodreads HTML scraping  
- Optional: HuggingFace models  
- Optional: Cloud storage for embeddings  

---

<a name="Architecture"></a>
## Architecture

### High‑Level Components
- **Frontend UI:** browsing, filtering, rating, tagging  
- **Backend API:** recommendation logic, metadata ingestion  
- **ML Pipeline:** embeddings, similarity scoring, clustering  
- **Database:** books, poems, embeddings, user preferences  
- **Optional Desktop Wrapper:** Electron or Flutter  

---

<a name="DataModels"></a>
## Data Models

### Book
- title  
- author  
- genres  
- description  
- ISBN  
- publication year  
- embedding  
- tags  
- ratings  

### Poem
- title  
- poet  
- era  
- themes  
- text (optional)  
- embedding  

### User
- reading history  
- ratings  
- taste vector  
- preference weights  

---

<a name="BasicWorkflow"></a>
## Basic Workflow

1. **Data Collection**
   - Import Goodreads/Kindle data.
   - User manually adds books/poems.
   - Fetch metadata from external APIs.

2. **Preprocessing**
   - Clean metadata.
   - Normalize genres, authors, themes.

3. **Feature Engineering**
   - Generate embeddings for books/poems.
   - Build user taste vector.

4. **Recommendation Engine**
   - Compute similarity scores.
   - Rank items.
   - Apply user preference weights.

5. **UI Interaction**
   - User browses recommendations.
   - Adjusts preferences.
   - Rates items to refine model.

---

<a name="BasicIO"></a>
## I/O Specifications

### Input
- Goodreads/Kindle exports  
- User ratings  
- User tags  
- Manual metadata edits  
- Preference weights  

### Output
- Ranked list of recommendations  
- Metadata panels  
- Taste vector summary  
- Optional exportable reading lists  

---

<a name="Implementation"></a>
## Implementation Guide

1. **Setup**
   - Install Python dependencies.
   - Install frontend dependencies.
   - Configure API keys.

2. **Backend**
   - Build ingestion pipeline.
   - Implement embedding generation.
   - Build recommendation endpoints.

3. **Frontend**
   - Create UI for browsing, filtering, rating.
   - Add metadata panels.
   - Add preference sliders.

4. **ML Pipeline**
   - Train or load embedding models.
   - Implement similarity scoring.
   - Build taste vector logic.

5. **Testing**
   - Unit tests for ingestion + ML.
   - UI tests for frontend.

6. **Deployment**
   - Web: deploy backend + frontend.
   - Desktop: package Electron app.

---

<a name="Roadmap"></a>
## Roadmap

### Phase 1 — Data Ingestion (2–3 weeks)
- Goodreads/Kindle import  
- Metadata fetching  
- Basic database schema  

### Phase 2 — Embeddings + ML (3–4 weeks)
- Embedding generation  
- Taste vector modeling  
- Similarity engine  

### Phase 3 — UI (3–4 weeks)
- Browsing interface  
- Metadata panels  
- Preference sliders  

### Phase 4 — Desktop App (optional) (2–3 weeks)
- Electron wrapper  
- Local storage  

### Phase 5 — Optimization + Deployment (2 weeks)

---

<a name="ToDo"></a>
## To‑Do List
- Build ingestion pipeline  
- Implement embeddings  
- Create similarity engine  
- Build UI  
- Add tagging system  
- Add exportable reading lists  
- Add desktop wrapper  

---

<a name="Timeline"></a>
## Estimated Timeline
10–14 weeks depending on scope.

---

<a name="Installation"></a>
## Installation

1. Clone repo  
2. Install Python deps  
3. Install frontend deps  
4. Configure API keys  
5. Run backend + frontend  

---

<a name="Usage"></a>
## Usage
- Import reading history  
- Generate recommendations  
- Adjust preferences  
- Rate items  

---

<a name="Contribute"></a>
## Contributions
Open to PRs.

---

<a name="Conclusion"></a>
## Conclusion
meta‑bookclub aims to provide a personalized, ML‑driven reading experience that adapts to user taste and evolves over time. With flexible architecture and support for both web and desktop implementations, it can scale from a simple recommender to a full literary discovery platform.

---

<a name="contact"></a>
## Contact
See GitHub profile.
