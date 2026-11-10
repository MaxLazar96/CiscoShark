# CiscoShark

A search engine for Cisco's technical documentation. It crawls Cisco documentation pages, builds a word index in the cloud, and lets users search it from a notebook-based web interface.

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/MaxLazar96/CiscoShark/blob/main/CiscoShark.ipynb)

> Team project for the Cloud Computing course, B.Sc. Software Engineering (Braude College), 4 students.
> **My part:** the back end: the crawler, the text-processing and indexing services, and the Firebase storage layer.


## How it works
1. **Crawl:** the search engine downloads Cisco documentation pages (Requests) and extracts their text (BeautifulSoup).
2. **Process:** a sentence-splitter service tokenizes the text and removes stop words.
3. **Index:** each term is stored in Firebase Realtime Database with the pages it appears on and a count.
4. **Search:** a query is split into terms and matched against the index to return the relevant pages.

## Features
- Keyword search over Cisco documentation
- Statistics page with a word cloud and charts of the indexed terms
- Admin page for managing the index, plus login and an About page
- Built-in assistant chatbot (Google Gemini API)

## Tech stack
| Area | Tools |
|---|---|
| Language | Python |
| Crawling and parsing | Requests, BeautifulSoup, NLTK / stop-words |
| Storage | Firebase Realtime Database |
| Interface | Google Colab, ipywidgets, Matplotlib, WordCloud |
| AI | Google Gemini API |

## Run it
1. Click **Open in Colab** above.
2. Add your own Gemini API key and Firebase database URL where the notebook asks for them.
3. Run the cells from top to bottom: installation, back end, then the front-end pages.
