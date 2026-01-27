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
      <li><a href="#tech">Currently Used Tech Stack</a></li>
      <li><a href="devenv">Development Environment</a></li>
      <li><a href="#uiux">UI/UX Implementation Details</a></li>
      <li><a href="io">Potential I/O Specifications</a>
      <li><a href="#err">Error Handling</a></li>
      <li><a href="#plus">Future Enhancements</a></li>
      <li><a href="bye">Conclusion</a></li>
    </ol>
  </details>
-
  <details>
    <summary><strong><em>II: Implementation Details</em></strong></summary>
    <ol>
      <li><a href="#tech">Technologies and Programming Languages</a></li>
      <li><a href="devenv">Development Environment</a></li>
      <li>
        <a href="#map">Roadmap</a>
        <ul>
          <li><a href="todo">To-Do List</a></li>
          <li><a href="est">Time Estimate</a></li>
        </ul> 
      </li>
      <li><a href="#uiux">UI/UX Implementation Details</a></li>
      <li><a href="#feat">Key Features</a></li>
      <li><a href="web">Web Application</a></li>
      <li><a href="#flow">Basic Workflow Guide</a></li>
      <li><a href="#impl">Project Implementation Guide</a></li>
      <li>
        <a href="io">Potential I/O Specifications</a>
        <ul>
          <li><a href="#i">Input</a></li>
          <li><a href="#o">Output</a></li>
          <li><a href="#err">Error Handling</a></li>
        </ul>
      </li>
      <li><a href="#plus">Future Enhancements</a></li>
    </ol>
  </details>
-
  <details>
    <summary><strong><em>III: Usage, Installation & Getting Started</em></strong></summary>
    <ol>
      <li>
        <a href="#view">Project Overview</a>
        <ul>
          <li><a href="#obj">Objectives</a></li>
        </ul>
      </li>
      <li><a href="#feat">Key Features</a></li>
      <li><a href="io">Potential I/O Specifications</a>
      <li><a href="#err">Error Handling</a></li>
      <li><a href="#install">Installation</a>
        <ul>
          <li><a href="#prereq">Prerequisites</a></li>
          <li><a href="buildnrun">Build and Run</a></li>
        </ul>
      </li>
      <li><a href="usage">Usage</a></li>
      <li><a href="#sys">System Requirements</a></li>
    </ol>
  </details>
-
  <details>
    <summary><strong><em>IV: Miscellaneous</em></strong></summary>
    <ol>
      <a href="#view">Project Overview</a>
      <li><a href="#tech">Technologies and Programming Languages</a></li>
      <li>
        <a href="misc">Miscellaneous</a>
          <ul>
            <li><a href="devenv">Development Environment</a></li>
            <li><a href="est">Time Estimate</a></li>
          </ul>
      </li>
      <li><a href="give">Contributions</a></li>
        <ul>
          <li><a href="coc">Code of Conduct</a></li>
          <li><a href="whattogive">What?</a></li>
          <li><a href="howtogive">How?</a></li>
          <li><a href="whygive">Why?</a></li>
        </ul>
      </li>><a href="Conclusion">Conclusion</a></li>
      <li><a href="#Contact">Contact</a></li>
      <li><a href="#Acknowledgements">Acknowledgments</a></li>
    </ol>
  </details>


- Current Tech Stack &nbsp; [<a href="#tech">view more details</a>]</p>


<details>
  <summary>Progress &nbsp; [<a href="#curr">view our progress, logs, and other documentation</a>]</summary>
    <p><strong><ins>Note</ins>:</strong><em> Last updated</em>: 1/27/26</p>
     <ol>
       <li><a href="080923">1/27/26</a></li>
     </ol>
  </summary>
</details>

### <ins>Table of Contents</ins>
- [Overview](#Overview)
    - [Objectives](#Objectives)
    - [Key Features](#KeyFeatures)
    - [Current Notes & Issues](#Notes)
- [Tech Stack](#TechStack)
- [Roadmap](#Roadmap)
- [MVP Scope (Personal Use)](#MVP)
- [Basic Workflow](#Workflow)
- [I/O Specifications](#IO)
- [Implementation Details](#Implementation)
- [Setup](#Setup)
- [Usage](#Usage)
- [Optional Future Enhancements](#Future)
- [Contributions](#Contributions)
- [Conclusion](#Conclusion)
- [Contact](#Contact)
- [Acknowledgments](#Acknowledgements)



---------------

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
- Optional advanced features (see below).


<p align="right">(<a href="#top">back to top</a>)</p>

---------------

<a name="Notes"></a>
## Current Notes & Issues


<p align="right">(<a href="#top">back to top</a>)</p>

---------------


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

  
<p align="right">(<a href="#top">back to top</a>)</p>


---------------

<a name="Roadmap"></a>
## Roadmap



<p align="right">(<a href="#top">back to top</a>)</p>

---------------


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

<a name="IO"></a>
## I/O Specifications

### Input
- Title, author, or tag  
- Local dataset (`books.json`)

### Output
- Ranked list of recommendations with similarity scores

<p align="right">(<a href="#top">back to top</a>)</p>

---------------

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
```

<p align="right">(<a href="#top">back to top</a>)</p>

---------------

<a name="Setup"></a>
## Setup


<p align="right">(<a href="#top">back to top</a>)</p>

---------------


<a name="Usage"></a>
## Usage


<p align="right">(<a href="#top">back to top</a>)</p>

---------------


<a name="Future"></a>
## Future


<p align="right">(<a href="#top">back to top</a>)</p>

---------------


<a name="Contributions"></a>
## Contributions


<p align="right">(<a href="#top">back to top</a>)</p>

---------------


<a name="Conclusion"></a>
## Conclusion


<p align="right">(<a href="#top">back to top</a>)</p>

---------------


<a name="Contact"></a>
## Contact


<p align="right">(<a href="#top">back to top</a>)</p>

---------------



<a name="Acknowledgements"></a>
## Acknowledgements


<p align="right">(<a href="#top">back to top</a>)</p>

---------------

