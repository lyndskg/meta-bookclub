<a name="top"></a>

<h1 align="center">meta-bookclub</h1>
<h4 align="center"><ins><strong><em>* a personal-use book + poem recommender with optional advanced features * </em></strong></ins></h4>

<p align="center">
  <a href="https://www.linkedin.com/in/lyndsey791/">LinkedIn</a> |
  <a href="https://github.com/lyndskg/">GitHub</a> |
  <a href="#contact">Contact</a>
</p>

---

## Contents
- [Overview](#Overview)
- [Objectives](#Objectives)
- [Key Features](#KeyFeatures)
- [Tech Stack](#TechStack)
- [MVP Scope (Personal Use)](#MVP)
- [Basic Workflow](#Workflow)
- [I/O Specifications](#IO)
- [Implementation Details](#Implementation)
- [Setup](#Setup)
- [Usage](#Usage)
- [Optional Future Enhancements](#Future)
- [Contact](#contact)

---

<a name="Overview"></a>
## Project Overview

`meta-bookclub` is a lightweight, personal-use AI-powered recommendation tool that generates personalized lists of suggested reading materials based on your own reading history. It uses a small local dataset, a pre-trained embedding model, and simple similarity scoring. Everything runs locally and privately. No accounts, no external APIs, no deployment, no UI requirements.

The base project is intentionally minimal. All advanced features are optional and can be added only if you want to.

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


---

<a name="KeyFeatures"></a>
## Key Features
- Local JSON dataset of books/poems.
- Pre-trained SentenceTransformer embeddings.
- Cosine similarity recommendations.
- Simple Python scripts (CLI or optional API).
- Fully offline and private.
- Optional advanced features (see below).

---

<a name="TechStack"></a>
## Tech Stack
**Core (MVP):**
- Python  
- SentenceTransformers  
- scikit-learn  
- JSON  

**Optional:**
- FastAPI (API wrapper)  
- React or simple HTML (UI)  
- SQLite/PostgreSQL (larger datasets)  

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

---

<a name="Workflow"></a>
## Basic Workflow

1. Add your books/poems to `books.json`.
2. Run `embed.py` to generate embeddings.
3. Run `recommend.py --title "<book>"`.
4. Get a ranked list of similar items.

---

<a name="IO"></a>
## I/O Specifications

### Input
- Title, author, or tag  
- Local dataset (`books.json`)

### Output
- Ranked list of recommendations with similarity scores

---

<a name="Implementation"></a>
## Implementation Details

### 1. Data
Example entry:

```json
{
  "title": "Bluets",
  "author": "Maggie Nelson",
  "genres": ["essay", "poetry"],
  "notes": "lyrical, fragmented, introspective"
}
