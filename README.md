# NCAA Baseball Knowledge Graph

A small knowledge graph of NCAA Division I college baseball rosters, built from public team websites and loaded into Neo4j.

## Project context

- Semester-long **graph database** project at **Temple University**  
- Course: Database / Graph Databases (graduate level)  
- Focus: designing an ontology, extracting data from multiple sources, and implementing a working Neo4j graph

## Tech stack

- **Neo4j AuraDB** – graph database and Cypher queries  
- **Cypher** – schema design and data loading  
- **Python** – web scraping and JSON generation  
- **APOC** – loading JSON into Neo4j (`apoc.load.json`)  
- **OWL / Protégé** – initial ontology sketch (conceptual model)

## What this project does

- Defines a **domain ontology** for college baseball:
  - `Player`, `Coach`, `SupportStaff`, `Team`, `School`, `Conference`, `Season`
  - Relationships such as `playsFor`, `coaches`, `worksFor`, `memberOf`, `participatesIn`
- Scrapes and normalizes **roster and staff data** from multiple NCAA Division I programs
- Exports a **clean JSON format** that matches the ontology
- Loads the data into Neo4j and creates a **unified knowledge graph** across schools and seasons
- Runs example queries, e.g.:
  - list players and their teams in a given season  
  - find coaching staff across multiple schools  
  - explore how teams connect to conferences and seasons

## Repository structure
My repo is not organized yet, but this is presentation of how I will want to organize it later:

- `data/` – cleaned JSON files per school (rosters, staff, relationships)
- `cypher/` – Cypher scripts to create constraints and load JSON into Neo4j  
- `ontology/` – OWL file and documentation of the final schema  
- `report/` – PDF report describing design decisions and evaluation (course deliverable)

## How to use

This repository is mainly intended as a **portfolio / academic project**:

- Open the Cypher scripts in Neo4j AuraDB to recreate the schema and load the data.
- Use the JSON files in `data/` together with `apoc.load.json` to populate the graph.
- The report and ontology files document the design decisions and mapping from raw HTML to the graph model.
