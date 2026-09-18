---
title: SQL Data Prep in Coworker
Metadata description: Learn how to use SQL Data Prep in Coworker to generate, optimize, troubleshoot, and schedule SQL queries.
---
# SQL Data Prep in Coworker

Brief overview:
- What SQL Data Prep is
- Why you would use it
- Relationship to Query Service / Data Distiller
- Accessed through Coworker

## Prerequisites

- Required product/license/access
- Required permissions
- Any Data Distiller requirement
- Any release/access restrictions

## Supported capabilities

Short summary table or list of the four capabilities.

### Generate SQL from natural language

Explain that Coworker can:
- Interpret a natural-language request
- Identify/validate relevant datasets
- Generate SQL
- Preview results
- Continue into save/schedule actions

Include one representative prompt.

### Optimize existing SQL

Explain that Coworker can:
- Accept existing SQL
- Optimize it for Data Distiller
- Preserve the intended result/business logic
- Explain changes and equivalence
- Optionally provide validation/EXPLAIN information

Include Sameeksha's optimization prompt.

### Diagnose and fix SQL errors

Explain that Coworker can:
- Analyze failing SQL
- Identify the likely root cause
- Produce corrected SQL
- Preview the corrected result

Include the supplied diagnostic prompt.

### Schedule SQL queries

Explain that Coworker can:
- Save and schedule a query
- Ask clarifying questions such as timezone
- Configure relevant query alerts

Probably one short prompt rather than a full workflow.

## Work with generated SQL

Potentially capture relevant common behavior:
- Preview is limited to five rows
- Generated SQL is already optimized
- Coworker may ask follow-up questions when information is missing
- Users can continue the conversation to preview, save, or schedule the query

## Example prompts

A compact set of representative prompts:
- SQL authoring
- SQL optimization
- Error diagnosis
- Scheduling

Possibly include one of the more transformation-oriented NL→SQL examples from the bug bash.

## Next steps

Links to:
- Query Service overview
- Data Distiller documentation
- Query Editor / schedules / alerts documentation as appropriate