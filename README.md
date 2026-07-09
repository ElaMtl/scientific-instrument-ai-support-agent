# Scientific Instrument AI Support Agent

**RAG-based AI support agent for technical customer inquiries at a scientific instrument manufacturer.**

The project focuses on requirements analysis, solution design, and architecture for an AI-assisted support system serving a small manufacturer of spectroscopy instruments used in research, industry, education, and applied science.

## Business Problem

Customer support depends heavily on a single domain expert who also manages sales, procurement, marketing, website operations, and product R&D.

A significant share of expert time is spent processing repetitive technical inquiries, searching historical emails and operational records, locating support materials, and preparing responses.

Key challenges:

- high dependency on a single subject matter expert;
- repetitive support requests and long response preparation time;
- knowledge concentrated in individual experience;
- fragmented and incomplete support materials;
- limited scalability and risk of inconsistent responses.

## Solution

The project designs a **Retrieval-Augmented Generation (RAG) support agent** that:

- classifies incoming customer inquiries;
- retrieves relevant information from approved knowledge sources;
- searches historical support emails and customer-specific order records;
- drafts grounded customer responses;
- locates drivers, calibration files, manuals, and technical documentation;
- routes complex or low-confidence cases to the domain expert;
- preserves source traceability and human oversight.

### High-Level Flow

**Customer Email → Classification → Retrieval → Response Drafting → Human Review / Automated Action**

Primary knowledge sources:

1. Historical sent emails
2. Order register
3. Product manuals and technical documentation

## Project Scope

### In Scope

- business process analysis;
- AS-IS and TO-BE process modelling;
- support inquiry classification design;
- knowledge base and retrieval requirements;
- RAG workflow design;
- functional and non-functional requirements;
- data model design;
- integration requirements;
- AI governance and escalation rules;
- use cases and acceptance criteria.

### Out of Scope

- full production implementation;
- enterprise CRM implementation;
- complete knowledge base migration;
- product development and R&D processes;
- sales, procurement, and marketing automation.

## Primary Stakeholder

### Business Owner / Subject Matter Expert

The business owner:

- provides product and technical support expertise;
- defines business priorities;
- validates requirements and proposed solutions;
- reviews generated responses when expert involvement is required;
- acts as the primary source of domain knowledge.

## MVP Design Decision

The initial version supports a **single primary request per email**.

Additional customer requests may be identified and stored as contextual information but do not trigger independent workflow execution. Routing is determined by the primary category and next action.

Multi-intent workflow orchestration is intentionally excluded from the MVP to reduce solution complexity.

The MVP does not introduce a new CRM or order management system. It uses existing operational data sources:

- email inboxes and historical sent emails;
- Google Sheets order records;
- Google Drive folders;
- product manuals and support documentation.

The data model defines the information objects required for classification, retrieval, response drafting, workflow execution, and source traceability.

## Repository Contents

- AS-IS and TO-BE process models
- Functional and non-functional requirements
- AI inquiry classification model
- RAG and retrieval design
- Data model
- Integration and sequence diagrams
- Use cases and acceptance criteria
- AI governance and escalation rules
- n8n workflow design

## Implementation Status

The current phase focuses on **requirements analysis, solution design, and architecture definition**.

An end-to-end n8n workflow may be implemented as a limited proof of concept in a future phase.
