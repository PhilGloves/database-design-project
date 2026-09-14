# Relational Database Design

University Database Systems project developed at the University of Turin.

The project covers the complete database design process for a platform
managing films, TV series, TV programs, cinemas, streaming platforms,
users, ratings and related entities.

## Project Scope

The work includes:

- Requirements analysis and domain modeling
- Conceptual E-R design
- Business rules and integrity constraints
- Workload and volume estimation
- Redundancy and performance trade-off analysis
- E-R schema restructuring
- Relational schema design
- PostgreSQL DDL implementation
- Database population through SQL DML

## Key Design Decision

One of the analyses evaluated whether the average user rating should be
computed dynamically or stored as a redundant attribute.

Based on the estimated workload, keeping the redundant value reduced the
estimated daily database accesses substantially while requiring negligible
additional storage.

## Repository Contents

- `Progetto Basi di Dati Guanti Filippo.pdf` — original university submission
- `sql/schema.sql` — SQL schema extracted from the original report
- `sql/sample-data.sql` — sample population statements extracted from the report

## Technologies

PostgreSQL · SQL · Relational Database Design · E-R Modeling

> This repository is a portfolio version of the original university project.
> The original submission was delivered as a single PDF document.
