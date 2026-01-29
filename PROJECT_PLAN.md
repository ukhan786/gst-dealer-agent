# Project Plan: Dealer Performance Analysis Agent

## Goal

Build an AI agent that can ingest and analyze complex Automotive Dealer performance data (financial statements, repair orders, sales efficiency, customer sales records, and business performance metrics) alongside dealer support manager (DSM) summaries and consulting manuals to produce data-backed observations and recommendations.

## Scope

### Data Inputs

- Financial statements (monthly/quarterly, departmental P&L, balance sheet, cash flow).
- Customer repair order (RO) data reports.
- Sales efficiency reports.
- Customer sales records.
- Business performance metrics dashboards.
- DSM dealer summary reports.
- Consulting manuals and operational playbooks.

### Outputs

- Executive summary of dealership health.
- KPI highlights with trends, variances, and benchmarks.
- Diagnostics with root-cause hypotheses.
- Data-backed recommendations and prioritized next steps.
- Appendix with supporting tables/figures.

## Key Requirements

- Read and normalize multi-sheet Excel files with inconsistent formatting.
- Create a canonical KPI schema and metric glossary.
- Map metrics to consultative model sections.
- Provide transparent citations to source data and assumptions.
- Support comparisons across time periods and peer benchmarks.
- Protect sensitive data and support redaction.

## Architecture Overview

1. **Ingestion Layer**
   - File intake for Excel, CSV, and PDF exports.
   - Schema detection and header normalization.
   - Versioning for datasets and transformations.
2. **Normalization & Modeling**
   - Canonical tables for financials, RO data, sales efficiency, and customer records.
   - Metric calculation engine with unit standardization.
   - Data quality checks (missing values, outliers, inconsistent totals).
3. **Knowledge Layer**
   - Consulting manuals and DSM summaries indexed for retrieval.
   - Glossary for KPI definitions and business logic.
4. **Analysis Engine**
   - Trend analysis, variance decomposition, and segmentation.
   - Correlation and diagnostic heuristics (e.g., tech efficiency vs. RO throughput).
5. **Recommendation Generator**
   - Evidence-backed recommendations linked to specific metrics.
   - Prioritized action list with expected impact.
6. **Reporting Layer**
   - Narrative summary with structured sections.
   - Tables and charts for key insights.

## Execution Plan

### Phase 1: Discovery & Data Mapping

- Collect representative samples of all report types.
- Build a data dictionary of common columns and KPI definitions.
- Identify gaps, inconsistencies, and required transformations.

### Phase 2: Ingestion & Normalization

- Implement Excel ingestion pipeline with schema inference.
- Build a canonical data model for key report categories.
- Create reusable transformations for known report templates.

### Phase 3: KPI Engine & Quality Checks

- Define KPI formulas and validation rules.
- Add data quality checks and anomaly detection.
- Establish benchmark comparisons (internal targets, OEM standards, peers).

### Phase 4: Knowledge Integration

- Index consulting manuals and DSM summaries for retrieval.
- Link KPIs to consultative framework sections and best practices.

### Phase 5: Analysis & Recommendation Layer

- Build analysis workflows for trends, variances, and segment insights.
- Generate recommendations with supporting evidence and citations.

### Phase 6: Reporting & Review

- Deliver a report template (summary, diagnostics, recommendations).
- Validate outputs with SME review and iterate.

## Milestones

- **M1:** Data inventory and report taxonomy complete.
- **M2:** Ingestion pipeline for core Excel reports.
- **M3:** KPI engine and validation suite.
- **M4:** Knowledge integration and consultative mapping.
- **M5:** End-to-end analysis report prototype.

## Risks & Mitigations

- **Inconsistent report formats:** Maintain template registry and fallback parsing.
- **Data quality issues:** Implement validation checks and flagging.
- **Metric ambiguity:** Maintain KPI glossary and require explicit mappings.
- **Recommendation accuracy:** Require evidence links and human review loop.

## Next Steps

- Gather sample reports and manuals.
- Draft initial KPI glossary.
- Define canonical schema and file intake conventions.
