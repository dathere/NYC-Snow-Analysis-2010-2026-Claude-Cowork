# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working in this repository.

## Project Overview

This is a **data analysis showcase repository** — not a software project. It demonstrates using Claude Cowork with MCP servers to analyze NYC's snow response from 2010–2026. The repo contains analysis outputs, reports, and transcripts; there is no build system, test suite, or application code.

The analysis combined six data sources: NYC 311 Service Requests (24.1GB, 42.8M rows), NYC DCP Housing Database (106K rows), US Census ACS data, Open-Meteo ERA5 weather data, NWS storm records, and news archives.

## Repository Structure

- `reports/` — Final deliverables: interactive HTML reports, Word documents (.docx), PowerPoint briefings (.pptx), and their PDF exports
- `qsv_generated/` — CSV/JSONL data files produced by the [qsv MCP Server](https://github.com/dathere/qsv) during analysis (stats caches, frequency tables, extracted subsets, weather data)
- `claude_cowork_generated/` — Cowork session artifacts including the compaction summary (`nyc_snow_analysis_COMPACTION.md`) documenting the mid-session context recovery
- `skills/genai-disclaimer/` — Custom Claude skill that adds AI-generated disclaimers to all document types (PPTX footers, DOCX footers, HTML footers, etc.). Used in the original analysis. Do not use this skill for content in this repo, as it may add disclaimers to the reports here which are meant to be static.
- `images/` — Visualization assets referenced by README
- `_config.yml` — GitHub Pages configuration (serves reports as a static site)

## Key Context

- The primary transcript is `claude_cowork_generated/nyc_snow_analysis-cowork_transcript.md` — it documents the full Cowork session workflow and task progression
- The `nyc_snow_analysis_COMPACTION.md` file preserves context from before Cowork's mid-session compaction, including all qsv queries, error resolutions, and data gathered
- Reports exist in multiple formats (HTML, DOCX, PPTX, PDF) — the HTML versions are the richest with interactive charts
- The GitHub Pages site at `dathere.github.io/NYC-Snow-Analysis-2010-2026-Claude-Cowork/` serves the README as the landing page with a Giscus comments widget

## MCP Servers Used in the Original Analysis

These are documented for context; they ran in Cowork, not in this repo:
- **qsv** — CSV data wrangling (indexing, stats, SQL queries via `qsv_sqlp` with Polars/DuckDB engines)
- **US Census Bureau Data API** — ACS 5-year demographic/economic data
- **Open-Meteo** — Historical weather data (ERA5 reanalysis)

