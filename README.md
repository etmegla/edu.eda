<a name="readme-top"></a>

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]



<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/AECinCode/edu.eda">
    <img src="assets/eda_cover.png" alt="Logo" width="30%">
  </a>

  <h3 align="center">Exploratory Data Analysis with OpenStreetMap</h3>

  <p align="center">
    A 3-day hands-on course: fetch real-world messy data, clean it with pandas, visualize it, and deploy a Streamlit app as a portfolio piece.
    <br />
    <a href="example/stockholm_eda.ipynb">Worked Example</a>
    ·
    <a href="exercises/">Exercises</a>
    ·
    <a href="docs/deploy.md">Deployment Guide</a>
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#about-the-course">About The Course</a></li>
    <li><a href="#learning-objectives">Learning Objectives</a></li>
    <li><a href="#schedule">Schedule</a></li>
    <li><a href="#prerequisites">Prerequisites</a></li>
    <li><a href="#getting-started">Getting Started</a></li>
    <li><a href="#repository-structure">Repository Structure</a></li>
    <li><a href="#the-dataset">The Dataset</a></li>
    <li><a href="#exercises">Exercises</a></li>
    <li><a href="#final-deliverable">Final Deliverable</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT THE COURSE -->
## About The Course

This is a practical EDA course built around **OpenStreetMap (OSM)** data — a massive, real-world, community-maintained geographic database with all the messiness that implies. There's no schema enforcement, tagging is by convention, and inconsistencies are everywhere.

Each student gets assigned a different city and works through the same pipeline:

1. **Fetch** raw data from the Overpass API
2. **Explore & clean** with pandas (wrong dtypes, duplicates, missing values, inconsistent tags)
3. **Visualize** with matplotlib and plotly (bar charts, interactive maps)
4. **Debug** intentionally broken code (read tracebacks, diagnose silent errors)
5. **Build** a Streamlit web app that presents your analysis
6. **Deploy** to Streamlit Community Cloud — a public URL you can put on your CV

The end result is a **portfolio piece**, not a notebook nobody ever opens again.

### Built With

* [pandas](https://pandas.pydata.org/) — data manipulation & cleaning
* [matplotlib](https://matplotlib.org/) — static visualizations
* [plotly](https://plotly.com/python/) — interactive charts & maps
* [Streamlit](https://streamlit.io/) — web app framework
* [Overpass API](https://overpass-api.de/) — OpenStreetMap data access

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- LEARNING OBJECTIVES -->
## Learning Objectives

By the end of this course you will be able to:

- Fetch structured data from a REST API and load it into a DataFrame
- Identify and fix common data quality issues (wrong dtypes, duplicates, missing values, inconsistent encoding)
- Normalize messy real-world tags into clean, analyzable columns
- Create both static and interactive visualizations to answer questions about data
- Read Python tracebacks and diagnose errors systematically
- Distinguish between exploration code (notebooks) and production code (`.py` files)
- Deploy a data application to the web

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- SCHEDULE -->
## Schedule

### Day 1 — Data Acquisition & Cleaning

| Time | Activity | Materials |
|------|----------|-----------|
| Morning | Intro to OSM + Overpass API, fetch your city's data | [Exercise 01](exercises/01_fetch_osm_data.ipynb) |
| Afternoon | Explore raw data, identify issues, clean & deduplicate | [Exercise 02](exercises/02_explore_and_clean.ipynb) |

**By end of day:** You have a clean DataFrame with proper dtypes, no duplicates, and extracted tag columns.

### Day 2 — Normalization, Visualization & Debugging

| Time | Activity | Materials |
|------|----------|-----------|
| Morning | Normalize tags (cuisine, opening_hours, names) | [Exercise 03](exercises/03_tag_normalization.ipynb) |
| Early afternoon | Visualize with matplotlib & plotly | [Exercise 04](exercises/04_visualization.ipynb) |
| Late afternoon | Debug intentionally broken code | [Exercise 05](exercises/05_debugging.ipynb) |

**By end of day:** You have normalized tags, publication-ready charts, and an interactive map. You can read a traceback.

### Day 3 — Streamlit App & Deployment

| Time | Activity | Materials |
|------|----------|-----------|
| Morning | Build your Streamlit app from notebook code | [Exercise 06](exercises/06_build_streamlit_app.md), [app.py template](app.py) |
| Afternoon | Deploy to Streamlit Community Cloud, present to class | [Deployment Guide](docs/deploy.md) |

**By end of day:** You have a live web app with a public URL. That's your portfolio piece.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- PREREQUISITES -->
## Prerequisites

- **Python basics** — variables, loops, functions, `import`. No pandas experience needed.
- **GitHub account** — you'll fork this repo and deploy from it.
- **A computer with Python 3.10+** installed.

No prior data analysis experience required. That's what this course teaches.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started

### 1. Fork & Clone

```bash
# Fork on GitHub first, then:
git clone https://github.com/YOUR_USERNAME/edu.eda.git
cd edu.eda
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Check Your City Assignment

Look up your assigned city in [docs/cities.md](docs/cities.md).

### 4. Open the First Exercise

```bash
jupyter notebook exercises/01_fetch_osm_data.ipynb
```

### Teacher Demo

The worked example for Stockholm is in [`example/stockholm_eda.ipynb`](example/stockholm_eda.ipynb) — use it as a reference, but try to solve the exercises yourself first.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- REPOSITORY STRUCTURE -->
## Repository Structure

```
edu.eda/
├── README.md                        ← you are here
├── requirements.txt                 ← Python dependencies
├── app.py                           ← Streamlit app template (Day 3)
│
├── example/
│   ├── stockholm_eda.ipynb          ← fully worked example (teacher reference)
│   └── app_stockholm.py            ← reference Streamlit app
│
├── exercises/
│   ├── 01_fetch_osm_data.ipynb      ← Day 1: fetch data from Overpass API
│   ├── 02_explore_and_clean.ipynb   ← Day 1: explore, clean, deduplicate
│   ├── 03_tag_normalization.ipynb   ← Day 2: normalize messy OSM tags
│   ├── 04_visualization.ipynb       ← Day 2: matplotlib + plotly charts & maps
│   ├── 05_debugging.ipynb           ← Day 2: diagnose intentionally broken code
│   └── 06_build_streamlit_app.md    ← Day 3: build & deploy instructions
│
├── docs/
│   ├── cities.md                    ← city assignments (one per student)
│   └── deploy.md                    ← Streamlit Community Cloud deployment guide
│
├── assets/                          ← course logo
└── data/                            ← (gitignored) your downloaded data goes here
```

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- THE DATASET -->
## The Dataset

**OpenStreetMap** is a free, community-maintained map of the world. Anyone can edit it. That's its strength — and the source of all the data quality issues you'll encounter:

| Problem | Example |
|---------|---------|
| Inconsistent tagging | `amenity=restaurant` vs `amenity=cafe` vs `amenity=fast_food` — no clear boundary |
| Multiple formats | Opening hours: `Mo-Fr 08:00-17:00` / `monday-friday 8-17` / `weekdays 8am-5pm` / empty |
| Multilingual names | `name`, `name:en`, `name:sv`, `name:ar` — which one to use? |
| Delimiter chaos | `cuisine=italian;pizza` vs `cuisine=Italian` vs `cuisine=Pizza, Italian` |
| Wrong dtypes | `building:levels="3"` (string) vs `3` (int), lat/lon as strings |
| Duplicates | Multiple nodes at the exact same coordinate |
| Deprecated tags | `highway=unsurfaced` (deprecated since 2008, still used) |
| Import artifacts | Mass imports with geometry errors, still not fully cleaned |

This is **not a toy dataset** — it's the real world, and that's the point.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- EXERCISES -->
## Exercises

| # | Notebook | Day | Style | Topic |
|---|----------|-----|-------|-------|
| 01 | [Fetch OSM Data](exercises/01_fetch_osm_data.ipynb) | 1 | Guided | Overpass API → JSON → DataFrame |
| 02 | [Explore & Clean](exercises/02_explore_and_clean.ipynb) | 1 | Guided | dtypes, NaN, duplicates, column extraction |
| 03 | [Tag Normalization](exercises/03_tag_normalization.ipynb) | 2 | Semi-guided | cuisine, opening_hours, multilingual names |
| 04 | [Visualization](exercises/04_visualization.ipynb) | 2 | Semi-guided | matplotlib bars + plotly interactive maps |
| 05 | [Debugging](exercises/05_debugging.ipynb) | 2 | Open-ended | Read tracebacks, fix intentionally broken code |
| 06 | [Build Streamlit App](exercises/06_build_streamlit_app.md) | 3 | Open-ended | Assemble notebook code into a deployed web app |

**Progressive difficulty:** exercises 01–02 are guided (fill in the blanks), 03–04 give you the problem and hints, 05–06 give you the problem and let you figure it out.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- FINAL DELIVERABLE -->
## Final Deliverable

Your deployed Streamlit app should include at minimum:

- **At least one filter** (e.g. dropdown to select amenity type)
- **An interactive map** showing your city's amenities
- **At least one chart** answering a question about your data
- **KPI metrics** (total amenities, unique types, data completeness, etc.)

The public URL is your portfolio piece. Ship it.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

* [OpenStreetMap contributors](https://www.openstreetmap.org/copyright)
* [Overpass API](https://overpass-api.de/)
* [Streamlit](https://streamlit.io/)
* [README template](https://github.com/othneildrew/Best-README-Template)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
[contributors-shield]: https://img.shields.io/github/contributors/AECinCode/edu.eda.svg?style=for-the-badge
[contributors-url]: https://github.com/AECinCode/edu.eda/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/AECinCode/edu.eda.svg?style=for-the-badge
[forks-url]: https://github.com/AECinCode/edu.eda/network/members
[stars-shield]: https://img.shields.io/github/stars/AECinCode/edu.eda.svg?style=for-the-badge
[stars-url]: https://github.com/AECinCode/edu.eda/stargazers
[issues-shield]: https://img.shields.io/github/issues/AECinCode/edu.eda.svg?style=for-the-badge
[issues-url]: https://github.com/AECinCode/edu.eda/issues
[license-shield]: https://img.shields.io/github/license/AECinCode/edu.eda.svg?style=for-the-badge
[license-url]: https://github.com/AECinCode/edu.eda/blob/main/LICENSE