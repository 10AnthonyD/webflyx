# Webflyx 🎬📚

**Webflyx** is a structured data repository and content organization system designed to manage, catalog, and store classic cinema titles, director logs, summaries, and famous quotes. 

This repository represents a foundational milestone project built while completing the backend engineering curriculum on [Boot.dev](https://boot.dev).

---

## 🚀 Features

* **Structured Data Catalog**: Utilizes structured CSV data (`classics.csv`) to cleanly map out cinema classics, directors, and release timelines.
* **Granular Text Aggregation**: Separates media listings (`titles.md`) and rich text overviews (`contents.md`) for flexible frontend parsing.
* **Curated Quote Engine**: Houses a dedicated sub-directory (`quotes/`) to organize, fetch, and isolate famous cinematic or script-based quotes.

---

## 📊 Data Schema (`classics.csv`)

The system indexes entries using a fixed, three-column schema. Be sure to match the specific structural headers exactly when appending new rows to the dataset:

| Column Header | Data Type | Description | Example Entry |
| :--- | :--- | :--- | :--- |
| `title` | String | The exact title of the cinematic or literary work. | *The Godfather* |
| `director` | String | The primary director or creator credited with the piece. | *Francis Ford Coppola* |
| `year` | Integer | The original theatrical or publishing release year. | *1972* |

---

## 🛠️ Tech Stack

* **Data Formats:** Markdown (`.md`), Comma-Separated Values (`.csv`)
* **Intended Compatibility:** Extensible with Python, Node.js, or any backend script capable of parsing file-system datasets.

---

## 📁 Repository Structure

```text
webflyx/
│
├── quotes/                # Directory containing structured or individual quote files
├── classics.csv           # Core dataset tracking titles, directors, and release years
├── contents.md            # Detailed summaries, descriptions, or long-form media content
├── titles.md              # Clean index of curated titles or media headers
└── README.md              # Project documentation
```

---

## 📦 Getting Started

### Usage and Integration

Because this repository acts as a clean, static data layout, you can consume its contents in your applications using standard file I/O operations.

#### Example: Parsing the Catalog with Python
You can read and iterate through the catalog data using Python's standard libraries:

```python
import csv

# Read and print the core classics catalog
with open('classics.csv', mode='r', encoding='utf-8') as file:
    reader = csv.DictReader(file)
    for row in reader:
        # Access elements matching the specific database schema
        print(f"Movie: {row['title']} | Directed By: {row['director']} ({row['year']})")
```

#### Example: Fetching Content Modules
You can build a quick wrapper script to read `titles.md` or parse through the `quotes/` folder to serve random daily quotes to an app UI, API endpoint, or terminal dashboard.

---

## 🧑‍💻 Contributing

As this is a foundational project for my [Boot.dev](https://boot.dev) portfolio, contributions are not actively being accepted, but feel free to fork the repository to experiment with your own static data-parsing features!
