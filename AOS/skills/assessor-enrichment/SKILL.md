---
name: assessor-enrichment
description: "Specialist for automated Assessor Enrichment processes. Takes raw property/tax data from local government assessors and enhances it with market valuations, ownership history, land-use details, zoning, units, and other metrics to create comprehensive property intelligence. Critical for voter file anomaly detection, permit analysis, construction oversight, and civic intelligence pipelines. Portable across U.S. jurisdictions. Triggers: 'assessor enrichment', 'property intelligence layer', 'assessor data join', 'enrich with assessor data', 'property anomaly validation'."
version: 1.0
---

# Assessor Enrichment Skill

## Overview
This skill provides a standardized, reproducible workflow for **Assessor Enrichment** — the automated process of taking raw property and tax data from local government assessors and enhancing it with additional metrics like market valuations, ownership history, land-use codes, number of units, improvement details, zoning context, and demographics to create comprehensive property intelligence.

It is designed for high-stakes applications such as voter registration anomaly detection (flagging implausible residential addresses), permit compliance validation, construction oversight, public records forensics, and broader civic intelligence work. Fully agnostic and portable for any U.S. county/jurisdiction.

## Core Principles
- **Evidence-First & Gate-First**: All enrichment must be validated against source data. Run quality gates before and after joins.
- **Efficiency**: Aggregate voter/records first → enrich only flagged/high-priority subsets (avoids processing millions of records unnecessarily).
- **Reproducibility**: Full audit logging, versioned data sources, deterministic joins (e.g., via AIN or standardized address keys).
- **Portable by Design**: Jurisdiction-agnostic patterns with examples for LA County, Florida counties, etc.
- **Court-Ready**: Outputs include provenance, confidence scores, and explicit Evidence/Inference labeling.

## When to Activate
Use this skill for:
- Enriching voter files with property data for anomaly detection (e.g., 15+ voters at commercial/vacant addresses).
- Permit or construction project validation against assessor records.
- Public records forensics involving real property.
- Building property intelligence layers in jurisdiction-ops or civic-intelligence-coordinator workflows.
- Any task requiring joining voter/registration data to assessor/parcel data.

## Activation Triggers
"assessor enrichment", "property intelligence layer", "assessor data join", "enrich with assessor data", "property anomaly validation", "assessor roll enrichment"

## Core Workflow
1. **Data Intake & Validation**:
   - Load raw assessor data (CSV, Parquet, shapefiles from county open data or bulk purchase).
   - Validate schema (AIN, land_use_code, address fields, assessed_value, etc.).
   - Run jurisdiction-ops gates if integrated.

2. **Standardization**:
   - Normalize addresses (USPS CASS or equivalent).
   - Create join keys (AIN primary; standardized address secondary).

3. **Enrichment Process**:
   - Join to primary dataset (e.g., voter file aggregates).
   - Pull/add fields: land_use_code, property_type (residential/commercial/vacant), units, ownership_history, market_value_estimate, zoning, year_built, etc.
   - Compute derived metrics: voter_density = voter_count / units (flag anomalies), value_per_unit, etc.

4. **Quality Gates & Anomaly Flagging**:
   - Flag implausible cases (e.g., single-family with voter_count >=15, commercial with high residential registrations).
   - Apply confidence scoring per join.
   - Log unmatched records.

5. **Output & Packaging**:
   - Enriched Parquet/CSV for field verification or further analysis.
   - GeoJSON for mapping.
   - Evidence manifest with provenance.

## Example DuckDB Implementation (LA County Style)
```sql
-- Aggregate voters first
CREATE TABLE voter_agg AS 
SELECT standardized_address, COUNT(DISTINCT voter_id) as voter_count, ...
FROM voter_file 
GROUP BY standardized_address;

-- Enrich with assessor
SELECT 
    va.*,
    a.land_use_code,
    a.property_type,
    a.assessed_value,
    a.units,
    CASE WHEN va.voter_count >= 15 AND a.property_type = 'single_family' THEN 'HIGH_ANOMALY' ELSE 'NORMAL' END as anomaly_flag
FROM voter_agg va
LEFT JOIN assessor_roll a ON va.ain = a.ain 
   OR va.standardized_address = a.standardized_address;
```

## Collaboration Patterns
- **With jurisdiction-ops**: Use as data quality layer for parcel/property corpora.
- **With public-records-forensics**: Enrich document analysis with parcel context.
- **With permit-coordinator / construction-oversight**: Validate site-level property intelligence.
- **With working-doc-manager**: Track enrichment metrics and decisions.
- **With oversight-kit-builder**: Package enriched findings for evidence kits.

## Deliverable Standards
- Enriched dataset with full provenance.
- Summary report: match rates, anomaly counts, confidence distribution.
- Explicit **Evidence** / **Inference** labeling.
- Reproducible script + run log.

## Anti-Patterns to Avoid
- Joining entire massive datasets without aggregation first.
- Using unverified or outdated assessor rolls.
- Blending raw and enriched data without clear versioning.
- Skipping USPS address standardization before joins.
- Making fraud claims without field verification.

## Integration Notes for AOS v2.1
- Add to Civic Intelligence / Public Records category in master-skill-index.
- Update solo-operator-playbook examples.
- Agnostic Edition ready: no location-specific identifiers.
