# 📊 DSI321 Final Project

## ✅ Project Status

| **Module / Tool**                            | **Status** |
|---------------------------------------------|:----------:|
| Modern Logging (`Logging`, `Rich`)          | ✅         |
| Web Scraping                                | ✅         |
| Database (`LakeFS`)                         | ✅         |
| Data Validation (`Pydantic`)                | ✅         |
| Orchestration (`Prefect`) Part 1: All tweets| ✅         |
| Orchestration (`Prefect`) Part 2: Only new tweets | ✅   |
| ML (`Word Cloud`)                           | ✅         |
| Web Interface (`Streamlit`)                 | ⬜️         |

---

## 🗂️ Project Structure

<details>
<summary>Click to expand</summary>

├── config
│ ├── docker
│ │ ├── Dockerfile.cli # CLI Dockerfile
│ │ └── Dockerfile.worker # Worker Dockerfile
│ ├── logging
│ │ └── modern_log.py # Custom logging with Rich
│ └── path_config.py # Paths config
├── src
│ ├── backend
│ │ ├── load
│ │ │ └── lakefs_loader.py # Upload to lakeFS
│ │ ├── pipeline
│ │ │ ├── initial_scrape_flow.py # First-time full scrape
│ │ │ └── incremental_scrape_flow.py # 15-min scrape flow
│ │ ├── scraping
│ │ │ ├── x_login.py # X login
│ │ │ └── x_scraping.py # Scraping logic
│ │ └── validation
│ │ └── validate.py # Pydantic data validation
│ └── fronend ← (typo! should be frontend)
│ └── streamlit.py # Streamlit dashboard
├── test # Test files
├── .env.example # Env variable example
├── .gitignore # Git ignore
├── README.md # Documentation
├── docker-compose.yml # Docker Compose setup
├── pyproject.toml # Poetry/Project config
├── requirements.txt # Required Python packages
└── start.sh # Startup script
