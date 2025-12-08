# AI-Powered SQL Generator for QGIS

A QGIS plugin that integrates a local AI model (Ollama) to convert natural-language questions into **PostgreSQL/PostGIS queries**, execute them directly on connected spatial datasets, and display the results inside QGIS.

This plugin allows GIS analysts to describe what they want in plain English, and have SQL generated automatically—ideal for spatial workflows, rapid querying, and learning SQL through examples.

---

## How it Works

1. User types a natural-language spatial analysis question.
2. Plugin fetches database schema.
3. Plugin sends prompt + schema to `http://localhost:11434/api/generate`.
4. Ollama returns SQL.
5. SQL preview is shown to the user.
6. User clicks **Execute**, and:
   - SQL runs in PostgreSQL,
   - Results are displayed in QGIS.

---

## Requirements

### QGIS
- QGIS 3.x

### Python Packages
- `psycopg2`
- `requests`

### Databases
- PostgreSQL
- PostGIS

### AI Model
- **Ollama** installed locally
- Model: `phi3` (or any model you choose)

