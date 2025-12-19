# Swiss Post – Postbox QA (early prototype)

This repository contains an **early QA prototype** to support the maintenance of
OpenStreetMap data for **letterboxes** (`amenity=post_box`) in Switzerland.

The project compares publicly available Swiss Post location data with existing
OpenStreetMap objects in order to **highlight potential discrepancies for human review**.

**No automated edits are performed.**

---

## Project status

- **Stage:** Early prototype
- **Scope:** Limited test areas (currently manual runs)
- **Automation:** None (results require human review)
- **Edits to OSM:** Performed manually by mappers only

A minimal project status page is published via GitHub Pages:

👉 https://swisspost-postbox-qa.github.io/worker/

---

## Purpose

The goal of this project is to provide **structured QA hints** to the OpenStreetMap community, such as:

- missing or outdated `collection_times`
- possible missing post_box objects in OSM
- OSM post_box objects that may require on-the-ground verification

Swiss Post data is used **as one input source only** and is **not treated as a single point of truth**.
OpenStreetMap remains the authoritative representation of on-the-ground reality.

---

## What this project is **not**

To avoid misunderstandings, this project is explicitly **not**:

- an automated edit or bot
- a data import into OpenStreetMap
- a replacement for local knowledge or surveys
- an authoritative source over OSM data

All suggested actions require **human judgement** by OSM mappers.

---

## Data sources

- **Swiss Post**  
  Public location search (Standortsuche)  
  Used for review and comparison only.

- **OpenStreetMap**  
  Data accessed via the Overpass API (`amenity=post_box`).

---

## Method (high-level)

1. Swiss Post letterbox locations are retrieved from public endpoints.
2. OSM `amenity=post_box` objects are retrieved via Overpass.
3. Objects are compared spatially using a fixed matching radius.
4. Differences are reported as **review candidates**, not edits.

Details may evolve as the prototype matures.

---

## Governance

This is a **community-driven project**.

- The repository is currently administered by the project initiator.
- The intention is to share maintenance responsibility with interested contributors.
- Ownership can be transferred or expanded to additional maintainers.

There is no affiliation with Swiss Post or the OpenStreetMap Foundation.

---

## Feedback & discussion

Feedback, critique and guidance from the OpenStreetMap community are very welcome.

Discussions are expected to happen primarily via:
- community.openstreetmap.org
- GitHub issues (for technical topics)

---

## License

The project code is published under an open-source license (to be specified).

Generated QA outputs are intended for community use.# worker
Tools to compare postbox objects in OSM and «Swiss Post Standortsuche»
