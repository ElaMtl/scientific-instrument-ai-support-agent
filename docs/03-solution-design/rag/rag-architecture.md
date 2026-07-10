# RAG Architecture

**Author:** Elvina Cherepovich  
**Role:** Technical Business Systems Analyst  
**Project:** AI Customer Inquiry Management Agent  
**Version:** Draft  
**Last Updated:** 2026-07-9

---

## 1. Purpose

This document defines the RAG architecture for an AI-assisted technical support system.

The solution combines:

- customer and instrument context retrieval;
- structured data lookup;
- technical knowledge retrieval;
- attachment analysis;
- multimodal AI analysis;
- response draft generation;
- clarification and expert escalation.

The system selects the processing path based on the customer request, attachment type, available context, and complexity of the technical question.

---

## 2. Scope

The project separates the complete target architecture from the limited MVP implementation.

### 2.1 Target Architecture

The target solution supports:

- incoming email processing;
- attachment detection and analysis;
- request classification;
- customer and instrument identification;
- retrieval from multiple information sources;
- technical attachment analysis;
- response draft generation;
- clarification requests;
- expert escalation;
- human review.

### 2.2 MVP Scope

The MVP focuses on two representative use cases:

1. Calibration File Recovery
2. Spectrum Troubleshooting

### 2.3 Implemented Vertical Slice

The primary implementation scenario is:

> **Spectrum Troubleshooting with Context-Grounded Draft Generation**

The system processes a customer email containing a spectrum-related attachment and prepares a response draft based on the attachment and retrieved technical context.

```text
Incoming Support Email
        ↓
Email and Attachment Intake
        ↓
Request and Attachment Analysis
        ↓
Customer and Instrument Context Retrieval
        ↓
Technical Knowledge Retrieval
        ↓
Spectrum Analysis
        ↓
Evidence Check
        ↓
Draft, Clarification, or Escalation
        ↓
Human Review
```

---

## 3. MVP Use Cases

### 3.1 Calibration File Recovery

A customer asks for a missing or replacement calibration file.

The system:

1. identifies the customer and instrument;
2. extracts available identifiers from the email;
3. searches the Order Register;
4. identifies the relevant serial number;
5. locates the calibration file;
6. verifies the match;
7. prepares a response draft;
8. attaches or links the file;
9. sends the draft for human review.

This use case validates structured data lookup, customer and instrument matching, file retrieval, and workflow automation.

### 3.2 Spectrum Troubleshooting

A customer sends a spectrum, measurement export, screenshot, or related technical attachment and asks why the result appears incorrect.

The system:

1. identifies the request as a technical support case;
2. detects and analyzes the attachment;
3. retrieves customer and instrument context;
4. retrieves relevant technical documentation and support knowledge;
5. analyzes the spectrum or measurement data;
6. combines the available evidence;
7. checks whether the information is sufficient;
8. prepares one of the following:
    - a response draft;
    - a clarification question;
    - an escalation package for the technical expert.

This use case validates multimodal analysis, cross-source retrieval, technical reasoning, and uncertainty handling.

---

## 4. Information Sources

The solution uses several information sources.

### Customer Email History

Used to retrieve:

- previous conversations;
- previous technical issues;
- customer-provided configuration details;
- previously sent instructions or files.

### Order Register

Used to retrieve:

- customer information;
- instrument model;
- serial number;
- order details;
- shipping information;
- calibration file reference.

### Technical Knowledge Base

Used to retrieve:

- product manuals;
- technical specifications;
- installation instructions;
- troubleshooting guidance;
- drivers and software information.

### Calibration Files

Used to locate the calibration data associated with a specific instrument.

### Customer Attachments

May include:

- spectrum images;
- measurement data;
- screenshots;
- spreadsheets;
- PDFs;
- setup photographs.

---

## 5. Request Routing

Different requests require different processing paths.

### Simple Information Request

Example:

> What is the wavelength range of this spectrometer?

```text
Request
→ Technical Knowledge Retrieval
→ Response Draft
```

### Calibration File Request

```text
Request
→ Customer Identification
→ Order Register Lookup
→ Instrument and Serial Number Match
→ Calibration File Retrieval
→ Verification
→ Response Draft
```

### Spectrum Troubleshooting Request

```text
Request and Attachment
→ Attachment Analysis
→ Customer and Instrument Context Retrieval
→ Technical Knowledge Retrieval
→ Spectrum Analysis
→ Evidence Check
→ Draft, Clarification, or Escalation
```

The routing decision depends on:

- request type;
- presence and type of attachment;
- customer and instrument context;
- required information sources;
- complexity of the technical question.

---

## 6. Evidence Check and Escalation

Before preparing a technical response, the system checks whether enough reliable information is available.

### Sufficient Evidence

The system prepares a grounded response draft for human review.

### Missing Information

The system prepares a clarification question.

Examples:

- instrument model is unknown;
- serial number is missing;
- measurement parameters are missing;
- attachment quality is insufficient.

### High Uncertainty

The system escalates the case to the technical expert.

The escalation package includes:

- customer request summary;
- identified customer and instrument context;
- relevant retrieved information;
- attachment analysis;
- unresolved questions.

### Conflicting Evidence

If retrieved sources or analysis results conflict, the system does not prepare a definitive technical answer and escalates the case for expert review.

---

## 7. RAG Processing Approach

The solution does not use the same retrieval process for every request.

The required processing may range from:

- direct retrieval of information from a technical document;
- structured lookup in the Order Register;
- retrieval across several information sources;
- analysis of technical attachments;
- synthesis of customer, instrument, and technical context;
- clarification or expert escalation when evidence is insufficient.

The target analysis pattern is:

```text
Customer Request
        +
Technical Attachment
        +
Customer and Instrument Context
        +
Calibration Context
        +
Technical Knowledge
        +
Relevant Support History
        ↓
Grounded Technical Support Draft
```

---

## 8. MVP Boundaries

### Included

- email intake;
- attachment detection;
- request classification;
- customer and instrument context retrieval;
- technical knowledge retrieval;
- calibration file recovery;
- controlled spectrum troubleshooting;
- response draft generation;
- clarification and escalation paths;
- human review.

### Excluded

- automatic sending of technical responses;
- definitive scientific diagnosis;
- autonomous warranty decisions;
- support for every spectroscopy file format;
- real-time instrument telemetry;
- automated instrument control;
- modification of calibration data;
- fully autonomous technical decision-making.

---

## 9. Evolution Roadmap

### Phase 1 — Reliable Retrieval

- calibration file recovery;
- driver and software retrieval;
- order and serial number lookup;
- standard product information.

### Phase 2 — Multimodal Technical Support

- spectrum images;
- screenshots;
- measurement exports;
- setup photographs;
- clarification question generation.

### Phase 3 — Cross-Source Technical Reasoning

- similar support case retrieval;
- customer history analysis;
- combined analysis across multiple sources;
- multiple possible cause identification.

### Phase 4 — Adaptive Processing

- dynamic selection of retrieval sources and analysis tools;
- repeated retrieval when information is missing;
- evidence completeness checks;
- alternative search strategies;
- advanced expert escalation.

---

## 10. Reference

The capability-based approach is informed by:

Gill, G., Gupta, R., Lusson, D., Chandrashekar, A., and Nguyen, D.  
_From Search to Reasoning: A Five-Level RAG Capability Framework for Enterprise Data._  
Technical Report, Corvic AI, 2025.  
arXiv:2509.21324.

The framework describes the progression from direct text retrieval to multi-source, multimodal, and adaptive reasoning. This project uses it as a design reference for request routing and future solution evolution.
