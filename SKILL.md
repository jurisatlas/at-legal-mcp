---
name: at-legal-mcp-skill
description: Official Austria (AT) legislation, multi-tier court precedent research, and citation verification skill.
version: 2.0.0
author: JurisAtlas
license: MIT
---

# Austria Legal Research & Multi-Tier Case Law Skill (`at-legal-mcp`)

Use this skill whenever the user asks a legal question, drafts a pleading or contract, or researches case law across any judicial instance in **Austria (AT)**.

## Verification & Research Rules

1. **Citation Verification:** Never fabricate a statutory provision or case citation. Query `search_legislation`, `search_case_law`, `search_tiered_court_decisions`, or `verify_citation` before citing any authority (e.g., `ECLI:AT:OGH0002:2024:0010OB00012.24A or BGBl. I Nr. 100/2023`).
2. **Multi-Tier Judicial Coverage:**
   - **First Instance (Trial / Municipal / District):** Bezirksgerichte (BG), Landesgerichte (LG), Handelsgericht Wien & Arbeits- und Sozialgericht Wien
   - **Second Instance (Cantonal / Regional / Appellate):** 4 Oberlandesgerichte (OLG Wien, Graz, Linz, Innsbruck), 9 Landesverwaltungsgerichte (LVwG), Bundesverwaltungsgericht (BVwG) & Bundesfinanzgericht (BFG)
   - **Supreme & Constitutional Instance:** Oberster Gerichtshof (OGH), Verfassungsgerichtshof (VfGH) & Verwaltungsgerichtshof (VwGH)
   - **Primary Tiered Database:** RIS BKA Judikatur API v2.6 (Justiz, VfGH, VwGH, BVwG, LVwG, BFG — data.bka.gv.at) (`https://data.bka.gv.at/ris/api/v2.6/Judikatur`)
