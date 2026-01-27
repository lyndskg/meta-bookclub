<a name="top"></a>

<h1 align="center">meta-bookclub</h1>
<h4 align="center"><ins><strong><em>* a personal-use book + poem recommender with optional advanced features * </em></strong></ins></h4>

<p align="center">
  <a href="https://www.linkedin.com/in/lyndsey791/">LinkedIn</a> |
  <a href="https://github.com/lyndskg/">GitHub</a> |
  <a href="#contact">Contact</a>
</p>

---------------


## Table of Contents

### I:  <ins>*Overview & Features*<ins>
- [Overview](#Overview)
    - [Objectives](#Objectives)
    - [Key Features](#KeyFeatures)
    - [Current Notes & Issues](#Notes)
- [Addenda](#Addenda)
    - [MVP Scope (Personal Use)](#MVP)
    - [Development Environment](#DevEnv)
    - [Time Estimate(s)](#TimeEst)
 
      
### II: *<ins>Implementation Details</ins>*
- [Tech Stack](#TechStack)
- [Roadmap](#Roadmap)
    - [To-Do List](#ToDo)
- [Basic Workflow](#Workflow)
- [Project Implementation Guide](#Project)
    - [Implementation Details](#Implementation)
    - [UI/UX Implementation Details](#UIUX)
    - [Web Application](#Web)
- [Optional Future Enhancements](#Future)
  
### III: *<ins>Usage, Installation & Getting Started</ins>*
- [I/O Specifications](#IO)
    - [Input](#i)
    - [Output](#o)
    - [Error Handling](#Error)
- [Installation](#Installation)
    - [Prerequisites](#Prereqs)
      - [System Requirements](#SystemReqs)
    - [Build & Run](#BuildAndRun)
- [Setup](#Setup)
- [Usage](#Usage)
  
### IV: *<ins>Miscellaneous</ins>*
- [Contributions](#Contributions)
- [Conclusion](#Conclusion)
- [Contact](#Contact)
- [Acknowledgments](#Acknowledgements)



---------------

<a name="Overview"></a>
## Project Overview

`meta-bookclub` is a lightweight, personal-use AI-powered recommendation tool that generates personalized lists of suggested reading materials based on your own reading history. It uses a small local dataset, a pre-trained embedding model, and cosine similarity scoring. Everything runs locally and privately. No accounts, no external APIs, no deployment, no UI requirements.

The base project is intentionally minimal. All advanced features are optional and can be added incremently &emdash; only if you want to.


&nbsp;

<a name="Objectives"></a>
## Objectives

The main objective of `meta-bookclub` is to enhance the reading experience of users by suggesting relevant books and poems that align with their unique interests and preferences.

- Load a small dataset of books/poems you’ve read or liked.
- Provide a simple, local recommendation tool.
- Use and enerate embeddings using a pre-trained model (no training required).
- Compute similarity between items.
- Return recommendations based on your taste.
- Keep the codebase small and easy to modify.
- Allow optional expansion into more advanced ML or UI features.

The system will continuously learn from user interactions and feedback, allowing it to improve and fine-tune its recommendations over time.

<p align="right">(<a href="#top">back to top</a>)</p>

---------------

<a name="KeyFeatures"></a>
## Key Features
- Local JSON dataset of books/poems.
- Pre-trained SentenceTransformer embeddings.
- Cosine similarity recommendations.
- Simple Python scripts (CLI or optional API).
- Fully offline and private.
- Optional advanced features (see Future Enhancements).


<p align="right">(<a href="#top">back to top</a>)</p>

---------------

<a name="Notes"></a>
## Current Notes & Issues
- Need to finalize JSON schema for books/poems.
- Need to choose embedding model (`all-mpnet-base-v2` recommended).
- No UI yet (optional).
- No metadata enrichment (optional).
- No Goodreads/Kindle import (optional).


<p align="right">(<a href="#top">back to top</a>)</p>

---------------
  
<a name="Addenda"></a>
## Addenda

---

<a name="MVP"></a>
## MVP Scope (Personal Use)

This is the version you can build in **1–2 sittings**.

### Included:
- `books.json` with your reading history  
- Embedding generation script  
- Similarity-based recommender  
- CLI or simple API endpoint  

### Not included (unless you want them):
- UI  
- External APIs  
- User accounts  
- ML training  
- Desktop app  
- Deployment  


<a name="DevEnv"></a>
## Development Environment
- `Python` 3.10+  
- Virtual environment recommended  
- macOS or Linux preferred (Windows works too)  
- `VSCode` or `PyCharm`  

<a name="TimeEst"></a>
## Time Estimate(s)
## Time Estimate(s)
- MVP: **2–4 hours**  
- Optional API: **1 hour**  
- Optional UI: **2–6 hours**  
- Optional metadata enrichment: **variable**  



<p align="right">(<a href="#top">back to top</a>)</p>

---------------


<a name="TechStack"></a>
## Tech Stack

### Core (MVP):
- `Python`  
- `SentenceTransformers` 
- `scikit-learn`  
- `JSON`  

### Optional:
- `FastAPI` (API wrapper)  
- `React` or simple HTML (UI)  
- `SQLite`/`PostgreSQL` (larger datasets)

  
<p align="right">(<a href="#top">back to top</a>)</p>


---------------

<a name="Roadmap"></a>
## Roadmap

1. Build MVP (JSON → embeddings → recommendations).  
2. Add optional FastAPI wrapper.  
3. Add optional UI.  
4. Add optional metadata enrichment.  
5. Add optional clustering / mood-based lists.  


<a name="ToDo"></a>
## To-Do List
- Finalize JSON schema  
- Implement `embed.py`  
- Implement `recommend.py`  
- Add CLI arguments  
- Add optional FastAPI endpoint  
- Add optional UI  
- Add optional metadata enrichment  

<p align="right">(<a href="#top">back to top</a>)</p>

---------------

<a name="Workflow"></a>
## Basic Workflow

1. Add your books/poems to `books.json`.
2. Run `embed.py` to generate embeddings.
3. Run `recommend.py --title "<book>"`.
4. Get a ranked list of similar items.


<p align="right">(<a href="#top">back to top</a>)</p>

---------------

<a name="Project"></a>
## Project Implementation Guide

1. Create `books.json`.  
2. Write embedding script.  
3. Write similarity script.  
4. Add CLI or API.  
5. (Optional) Add UI. 

---

<a name="Implementation"></a>
## Implementation Details

### 1. Data Example
```json
{
  "title": "Bluets",
  "author": "Maggie Nelson",
  "genres": ["essay", "poetry"],
  "notes": "lyrical, fragmented, introspective"
}
```


<a name="UIUX"></a>
## UI/UX Implementation Details

The MVP does not require a UI, but if you choose to add one later, the structure is simple:

- A single search input for entering a book/poem title.
- A results panel listing recommended items with similarity scores.
- Optional metadata display (author, genres, notes).
- Optional tag editor for refining personal preferences.
- Minimal styling; functionality is the priority.

The UI can be implemented as:
- A static HTML page calling a FastAPI endpoint, or
- A small React component with a single route.


<a name="Web"></a>
## Web Application

The web version is optional. If implemented:

**Backend (FastAPI):**
- Endpoint: `/recommend?title=<title>`
- Returns JSON list of recommendations.
- Loads precomputed embeddings from disk.

**Frontend (optional):**
- Simple fetch request to the backend.
- Displays ranked recommendations.
- No authentication or persistent user accounts.

This keeps the web version lightweight and easy to maintain.


<p align="right">(<a href="#top">back to top</a>)</p>

---------------

<a name="Future"></a>
## Optional Future Enhancements

These are optional and can be added incrementally:

### Data & Metadata
- Goodreads/Kindle import.
- `OpenLibrary` / Google Books metadata enrichment.
- Automatic genre/theme extraction.
- Author similarity graphs.

### ML / Recommendation Logic
- Hybrid recommender (content + collaborative filtering).
- Mood‑based clustering.
- Personalized taste vector with adjustable weights.
- Re-ranking based on user feedback.

### UI / UX
- Tagging interface.
- Reading dashboard with stats.
- Saved lists and collections.
- “If you liked X, you’ll like Y” chains.

### Storage / Scaling
- `SQLite`/`PostgreSQL` database.
- Cached embeddings for faster lookup.
- Support for larger datasets.

All enhancements are optional and do not affect the MVP.

<p align="right">(<a href="#top">back to top</a>)</p>

---------------


<a name="IO"></a>
## I/O Specifications

<a name="i"></a>
### Input
- Title, author, or tag.
- Local dataset (`books.json`).
- Optional: user-provided notes or tags.

<a name="o"></a>
### Output
- Ranked list of recommendations with similarity scores.
- Optional metadata (author, genres, notes).


<a name="Error"></a>
### Error Handling
- Title not found in dataset → return a clear message.
- Empty dataset → instruct user to populate `books.json`.
- Embedding file missing → instruct user to run `embed.py`.
- Invalid JSON format → prompt user to fix malformed entries.



<p align="right">(<a href="#top">back to top</a>)</p>

---------------


<a name="Installation"></a>
## Installation

<a name="Prereqs"></a>
### Prerequisites
- `Python` 3.10+
- `pip`
- Basic familiarity with running Python scripts
  

<a name="SystemReqs"></a>
#### System Requirements
- macOS, Linux, or Windows
- ~200MB disk space for embedding model
- No GPU required

<a name="BuildAndRun"></a>
### Build & Run
```bash
pip install -r requirements.txt
python embed.py
python recommend.py --title "Normal People"
```

<p align="right">(<a href="#top">back to top</a>)</p>

---------------

<a name="Setup"></a>
## Setup
1. Clone the repository.
2. Create and activate a virtual environment (optional).
3. Install dependencies.
4. Add your books/poems to `books.json`.
5. Run `embed.py` to generate embeddings.
6. Run `recommend.py` to get recommendations.


<p align="right">(<a href="#top">back to top</a>)</p>

---------------

<a name="Usage"></a>
## Usage


Example:
```
python recommend.py --title "Bluets"
```

Example output:
```
1. The Argonauts (0.82)
2. On Earth We're Briefly Gorgeous (0.79)
3. Night Sky With Exit Wounds (0.76)
```


<p align="right">(<a href="#top">back to top</a>)</p>

---------------

<a name="Misc"></a>
## Miscellaneous

This project is intentionally minimal.

All advanced features are optional and can be added only if desired.


<a name="Contributions"></a>
## Contributions

Contributions are welcome.

Focus areas:
• Code cleanup
• Additional metadata fields
• Optional UI components
• Optional API improvements

<p align="right">(<a href="#top">back to top</a>)</p>

---------------


<a name="Conclusion"></a>
## Conclusion

`meta-bookclub` provides a simple, local recommendation tool that can be expanded over time.

The MVP is small and fast to build; advanced features are modular and optional.

<p align="right">(<a href="#top">back to top</a>)</p>

---------------


<a name="Contact"></a>
## Contact

See GitHub profile for links and communication options.

<p align="right">(<a href="#top">back to top</a>)</p>

---------------



<a name="Acknowledgements"></a>
## Acknowledgements

- `SentenceTransformers`
- `scikit-learn`
- Open-source ML community

<p align="right">(<a href="#top">back to top</a>)</p>

---------------


## Contents

-
  <details>
    <summary><strong><em>I: Overview & Features</em></strong></summary>
    <ol>
      <li>
        <a href="#Overview">Project Overview</a>
        <ul>
          <li><a href="#Objectives">Objectives</a></li>
          <li><a href="#KeyFeatures">Key Features</a></li>
          <li><a href="#Notes">Current Notes and Issues</a></li>
        </ul>
      </li>
    </ol>
  </details>
-
  <details>
    <summary><strong><em>II: Implementation Details</em></strong></summary>
    <ol>
      <li><a href="#TechStack">Technologies and Programming Languages</a></li>
      <li>
        <a href="#Roadmap">Roadmap</a>
        <ul>
          <li><a href="#Todo">To-Do List</a></li>
        </ul> 
      </li>
      <li><a href="#MVP">MVP Scope (Personal Use)n</a></li>
      <li><a href="#Workflow">Basic Workflow Guide</a></li>
      <li>
        <a href="#Project">Project Implementation Guide</a></li>
      <ul>
      <li><a href="#UIUX">UI/UX Implementation Details</a></li>
      <li><a href="#Web">Web Application</a></li>
      <li><a href="#Implementation">Implementation Details</a></li>
      </ul>
      <li><a href="#Future">Future Enhancements</a></li>
    </ol>
  </details>
-
  <details>
    <summary><strong><em>III: Usage, Installation & Getting Started</em></strong></summary>
    <ol>
      <li>
        <a href="#IO">I/O Specifications</a>
        <ul>
          <li><a href="#i">Input</a></li>
          <li><a href="#o">Output</a></li>
          <li><a href="#Error">Error Handling</a></li>
        </ul>
      </li>
      <li><a href="#Install">Installation</a>
        <ul>
          <li><a href="#Prereqs">Prerequisites</a></li>
          <li><a href="#BuildAndRun">Build and Run</a></li>
        </ul>
      </li>
      <li><a href="#Setup">Setup</a></li>
      <li><a href="#Usage">Usage</a></li>
      <li><a href="#SystemReqs">System Requirements</a></li>
    </ol>
  </details>
-
  <details>
    <summary><strong><em>IV: Miscellaneous</em></strong></summary>
    <ol>
      <li>
        <a href="Misc">Miscellaneous</a>
          <ul>
            <li><a href="#DevEnv">Development Environment</a></li>
            <li><a href="#TimeEst">Time Estimate</a></li>
          </ul>
      </li>
      <li><a href="Contributions">Contributions</a></li>
      <li><a href="Conclusion">Conclusion</a></li>
      <li><a href="Contact">Contact</a></li>
      <li><a href="Acknowledgements">Acknowledgments</a></li>
    </ol>
  </details>

<details>
  <summary>File Hierarchy</summary>
</details>

<details>
  <summary>Current Tech Stack &nbsp; [<a href="#TechStack">view more details</a>]</p>
  </summary>
</details>


<details>
  <summary>Progress &nbsp; [<a href="#curr">view our progress, logs, and other documentation</a>]</summary>
    <p><strong><ins>Note</ins>:</strong><em> Last updated</em>: 1/27/26</p>
     <ol>
       <li><a href="080923">1/27/26</a></li>
     </ol>
  </summary>
</details>

