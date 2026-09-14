# Relational Database Design – Cinema & TV Platform

University project developed for the Database Systems course at the University of Turin.

The goal of the project was to design and implement a relational database for a media platform providing information about films, TV series, TV programs, cinemas and streaming platforms.

The work covered the complete database design process, from requirements analysis and conceptual modeling to relational schema design and SQL implementation.

## Project Overview

The database models several interconnected areas of a media platform, including:

- films, TV series and TV programs
- seasons and episodes
- actors and directors
- cinemas and film screenings
- TV channels and streaming platforms
- registered users and editors
- ratings and favorite content

The project started from a set of application requirements and progressively developed them into an E-R model, business rules, a restructured conceptual schema and finally a relational database implementation.

## Main Topics

### Requirements Analysis

The initial requirements were reviewed and reorganized into homogeneous groups in order to identify the main entities, relationships, attributes and application constraints.

### E-R Modeling

An initial Entity-Relationship schema was designed to represent the domain.

The schema was later restructured by:

- resolving entity generalizations
- transforming multivalued attributes
- restructuring composite attributes
- selecting primary identifiers
- introducing additional business rules

### Workload and Volume Analysis

Estimated entity volumes and application operations were defined in order to evaluate the expected database workload.

The analysis considered both read-intensive operations, such as retrieving information about films and TV series, and write operations such as adding ratings and users.

### Redundancy Analysis

One of the main design decisions concerned whether the average user rating of a piece of content should be calculated dynamically or stored as a derived attribute.

Under the workload assumptions used in the project:

- maintaining the derived value resulted in approximately **19.9 million estimated database accesses per day**
- calculating the value dynamically resulted in approximately **1.97 billion estimated accesses per day**

The derived value was therefore retained, trading a very small amount of additional storage for a substantially lower estimated read cost.

> These figures are based on the workload assumptions defined for the academic project and are intended as a database design exercise rather than measurements from a production system.

### Relational Design

The restructured E-R model was translated into a relational schema containing entities and relationships for users, content, artists, cinemas, platforms, ratings, screenings, seasons and episodes.

Referential integrity rules were defined using primary keys, foreign keys and different deletion/update strategies according to the semantics of each relationship.

Examples include:

- `ON DELETE CASCADE`
- `ON DELETE SET NULL`
- `ON UPDATE CASCADE`
- value constraints using `CHECK`

### SQL Implementation

The final database was implemented in SQL and tested using PostgreSQL.

The implementation includes:

- table creation
- primary and foreign keys
- integrity constraints
- referential actions
- sample data population

## Technologies

- PostgreSQL
- SQL
- Relational Database Design
- Entity-Relationship Modeling
- Data Modeling
- Database Workload Analysis

## Original University Report

The complete original submission is available in Italian:

[View the original project report](./Progetto%20Basi%20di%20Dati%20Guanti%20Filippo.pdf)

The report contains the complete requirements analysis, E-R diagrams, workload calculations, design decisions, relational schema, SQL DDL and sample data.

> The original report is preserved as submitted for the university course. This README provides an English overview for portfolio purposes.
