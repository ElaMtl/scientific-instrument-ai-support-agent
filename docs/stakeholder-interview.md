# AI Support Assistant - Discovery Questions

## 1. Which support requests should never be answered automatically?

### Question

Which categories of inquiries must always be reviewed by you or another expert before a response is sent?

### Why

Not all support requests carry the same risk.

Examples:

- instrument configuration recommendations;
- experimental methodology;
- calibration procedures;
- warranty disputes;
- custom engineering requests.

### Impact

Defines:

- escalation rules;
- AI boundaries;
- human review requirements.

### Scores

| Criterion                  | Score |
| -------------------------- | ----- |
| Requirements clarification | 10    |
| Impact on architecture     | 10    |
| Risk identification        | 10    |
| Practical value            | 10    |

---

## 2. Does the correct answer depend on the instrument version?

### Question

Can the same customer question have different answers depending on the instrument model, hardware revision, firmware version, software version, or manufacturing date?

### Why

This determines whether the AI can answer using generic documentation or must identify the exact product configuration first.

### Impact

Defines:

- data model;
- product metadata requirements;
- retrieval strategy.

### Scores

| Criterion                  | Score |
| -------------------------- | ----- |
| Requirements clarification | 10    |
| Impact on architecture     | 10    |
| Risk identification        | 10    |
| Practical value            | 10    |

---

## 3. Where does critical knowledge exist today?

### Question

What information do you use when answering customers that is not stored in manuals, documentation, or any searchable system?

### Why

In small engineering companies, valuable knowledge often exists only:

- in the owner's head;
- in old emails;
- in chat messages;
- in laboratory notes.

### Impact

Defines:

- knowledge acquisition strategy;
- knowledge base scope;
- project feasibility risks.

### Scores

| Criterion                  | Score |
| -------------------------- | ----- |
| Requirements clarification | 10    |
| Impact on architecture     | 10    |
| Risk identification        | 10    |
| Practical value            | 10    |

---

## 4. What should happen when the AI is uncertain?

### Question

If the AI cannot find a reliable answer, what is the preferred action?

Options may include:

- ask clarification questions;
- escalate to an expert;
- provide partial guidance;
- decline to answer.

### Why

Every AI support system spends most of its lifecycle handling uncertainty.

### Impact

Defines:

- fallback workflows;
- orchestration logic;
- customer experience.

### Scores

| Criterion                  | Score |
| -------------------------- | ----- |
| Requirements clarification | 10    |
| Impact on architecture     | 10    |
| Risk identification        | 9     |
| Practical value            | 10    |

---

## 5. What customer attachments must the AI understand?

### Question

What file types do customers typically send when requesting support?

Examples:

- spectra;
- screenshots;
- photographs;
- CSV exports;
- instrument logs;
- configuration files.

### Why

Support requests often depend more on attached files than on the email text.

### Impact

Defines:

- document processing requirements;
- multimodal capabilities;
- future roadmap.

### Scores

| Criterion                  | Score |
| -------------------------- | ----- |
| Requirements clarification | 10    |
| Impact on architecture     | 10    |
| Risk identification        | 9     |
| Practical value            | 10    |

---

## 6. Which source should be trusted when information conflicts?

### Question

If documentation, historical emails, specifications, and personal expertise provide different answers, which source takes priority?

### Why

Conflicting knowledge is common in engineering environments.

### Impact

Defines:

- retrieval ranking;
- governance rules;
- knowledge management processes.

### Scores

| Criterion                  | Score |
| -------------------------- | ----- |
| Requirements clarification | 10    |
| Impact on architecture     | 10    |
| Risk identification        | 10    |
| Practical value            | 10    |

---

## 7. What level of technical risk is acceptable?

### Question

What is worse for the business:

- providing no answer;
- providing a delayed answer;
- providing an incorrect answer?

### Why

The answer determines how conservative the system should be.

### Impact

Defines:

- confidence thresholds;
- approval workflow;
- automation level.

### Scores

| Criterion                  | Score |
| -------------------------- | ----- |
| Requirements clarification | 9     |
| Impact on architecture     | 10    |
| Risk identification        | 10    |
| Practical value            | 10    |

---

## 8. Which support requests are actually sales opportunities?

### Question

Which support conversations frequently lead to:

- accessory sales;
- upgrades;
- replacement components;
- service contracts;
- new instrument purchases?

### Why

Many technical inquiries are hidden commercial opportunities.

### Impact

Defines:

- CRM integration requirements;
- lead identification rules;
- business value metrics.

### Scores

| Criterion                  | Score |
| -------------------------- | ----- |
| Requirements clarification | 8     |
| Impact on architecture     | 9     |
| Risk identification        | 7     |
| Practical value            | 10    |

---

## 9. Who will maintain the knowledge base after deployment?

### Question

Who will be responsible for keeping technical content accurate and up to date?

### Why

Most AI support projects fail because knowledge becomes outdated.

### Impact

Defines:

- content management process;
- ownership model;
- administration requirements.

### Scores

| Criterion                  | Score |
| -------------------------- | ----- |
| Requirements clarification | 10    |
| Impact on architecture     | 9     |
| Risk identification        | 10    |
| Practical value            | 10    |

---

## 10. What would make you consider the project a failure six months after launch?

### Question

What outcomes would make you conclude that the solution is not delivering value?

Examples:

- incorrect answers;
- low adoption;
- excessive review effort;
- outdated content;
- customer complaints.

### Why

Failure criteria are often clearer than success criteria.

### Impact

Defines:

- project KPIs;
- acceptance criteria;
- reporting requirements.

### Scores

| Criterion                  | Score |
| -------------------------- | ----- |
| Requirements clarification | 9     |
| Impact on architecture     | 8     |
| Risk identification        | 10    |
| Practical value            | 10    |

# Email Operations, Documentation, and Support Metrics Discovery Questions

## 11. What is the actual monthly support volume?

### Question

How many support emails do you receive per week and per month?

Please estimate:

- total emails;
- technical support requests;
- sales inquiries;
- spam and irrelevant emails.

### Why

Many automation projects are proposed before validating the volume.

### Impact

Defines:

- project ROI;
- infrastructure sizing;
- MVP justification.

### Scores

| Criterion                  | Score |
| -------------------------- | ----- |
| Requirements clarification | 10    |
| Impact on architecture     | 8     |
| Risk identification        | 9     |
| Practical value            | 10    |

---

## 12. Which inquiries consume the most time?

### Question

Which 5 inquiry types consume the most time, regardless of how often they occur?

### Why

High-frequency requests and high-effort requests are not always the same.

### Impact

Defines:

- automation priorities;
- training dataset priorities;
- business value.

### Scores

| Criterion                  | Score |
| -------------------------- | ----- |
| Requirements clarification | 10    |
| Impact on architecture     | 8     |
| Risk identification        | 8     |
| Practical value            | 10    |

---

## 13. What percentage of replies are written from scratch?

### Question

For a typical week, what percentage of responses are:

- copied from previous emails;
- adapted from templates;
- written entirely from scratch?

### Why

This helps determine how much reusable knowledge already exists.

### Impact

Defines:

- template strategy;
- knowledge extraction approach;
- AI response generation requirements.

### Scores

| Criterion                  | Score |
| -------------------------- | ----- |
| Requirements clarification | 10    |
| Impact on architecture     | 9     |
| Risk identification        | 8     |
| Practical value            | 10    |

---

## 14. Do customers expect responses in multiple languages?

### Question

What languages are used in customer communications, and what percentage of emails arrives in each language?

### Why

Language support can significantly affect model selection and testing.

### Impact

Defines:

- multilingual requirements;
- prompt strategy;
- evaluation criteria.

### Scores

| Criterion                  | Score |
| -------------------------- | ----- |
| Requirements clarification | 9     |
| Impact on architecture     | 8     |
| Risk identification        | 7     |
| Practical value            | 9     |

---

## 15. How important is the owner's writing style?

### Question

Should AI responses sound exactly like you, or is technical accuracy more important than maintaining your personal communication style?

### Why

Some founders view communication style as part of the brand.

### Impact

Defines:

- prompt engineering requirements;
- response templates;
- review expectations.

### Scores

| Criterion                  | Score |
| -------------------------- | ----- |
| Requirements clarification | 8     |
| Impact on architecture     | 7     |
| Risk identification        | 6     |
| Practical value            | 8     |

---

## 16. What information do you always look for before answering?

### Question

When reading a support email, what information do you immediately try to identify before drafting a response?

Examples:

- instrument model;
- software version;
- customer type;
- application domain;
- attached files.

### Why

This often reveals hidden business rules.

### Impact

Defines:

- entity extraction requirements;
- email analysis workflow;
- metadata model.

### Scores

| Criterion                  | Score |
| -------------------------- | ----- |
| Requirements clarification | 10    |
| Impact on architecture     | 10    |
| Risk identification        | 9     |
| Practical value            | 10    |

### Example Answer

First, I identify the instrument model. Then I check what exactly the customer is trying to do. After that I look at any screenshots, spectra, logs, or photos they attached. Many problems cannot be diagnosed without this context.

---

## 17. How often do customers fail to provide enough information?

### Question

What percentage of support requests require follow-up questions before a meaningful answer can be provided?

### Why

This determines whether clarification workflows are a primary use case.

### Impact

Defines:

- conversational workflow;
- clarification templates;
- process complexity.

### Scores

| Criterion                  | Score |
| -------------------------- | ----- |
| Requirements clarification | 10    |
| Impact on architecture     | 9     |
| Risk identification        | 9     |
| Practical value            | 10    |

### Example Answer

Around 50–70% of technical support requests require at least one follow-up question. Customers often describe symptoms but do not provide the instrument model, software version, or relevant screenshots.

---

## 18. How good is the existing documentation?

### Question

If you had to rate your current documentation on a scale from 1 to 10, what score would you give it and why?

### Why

AI quality depends heavily on source content quality.

### Impact

Defines:

- knowledge preparation effort;
- project risks;
- implementation timeline.

### Scores

| Criterion                  | Score |
| -------------------------- | ----- |
| Requirements clarification | 9     |
| Impact on architecture     | 9     |
| Risk identification        | 10    |
| Practical value            | 10    |

---

## 19. How often does documentation become outdated?

### Question

How frequently do product specifications, manuals, procedures, or troubleshooting instructions change?

### Why

Knowledge freshness requirements affect architecture decisions.

### Impact

Defines:

- update mechanisms;
- synchronization requirements;
- governance model.

### Scores

| Criterion                  | Score |
| -------------------------- | ----- |
| Requirements clarification | 9     |
| Impact on architecture     | 9     |
| Risk identification        | 10    |
| Practical value            | 10    |

---

## 20. How do you currently find answers?

### Question

When you do not remember an answer, where do you look first?

Examples:

- manuals;
- previous emails;
- local files;
- Google Drive;
- source code;
- laboratory notes.

### Why

Current behavior often reveals the future retrieval architecture.

### Impact

Defines:

- source systems;
- knowledge repositories;
- ingestion scope.

### Scores

| Criterion                  | Score |
| -------------------------- | ----- |
| Requirements clarification | 10    |
| Impact on architecture     | 10    |
| Risk identification        | 9     |
| Practical value            | 10    |

### Example Answer

## Usually I search previous emails first because many similar questions have already been answered. Then I check manuals, technical notes, product specifications, and sometimes source code or laboratory test results.

## 21. What is your current response-time target?

### Question

How quickly do customers expect a response, and how quickly do you actually respond today?

### Why

Perceived service quality is often tied to response time.

### Impact

Defines:

- SLA requirements;
- automation urgency;
- success metrics.

### Scores

| Criterion                  | Score |
| -------------------------- | ----- |
| Requirements clarification | 9     |
| Impact on architecture     | 8     |
| Risk identification        | 8     |
| Practical value            | 10    |

---

## 22. Which support metrics matter to you?

### Question

Which metrics would convince you that the project is successful?

Examples:

- fewer hours spent on email;
- faster response times;
- fewer repeat questions;
- higher customer satisfaction;
- increased sales opportunities.

### Why

Many projects start without measurable outcomes.

### Impact

Defines:

- KPIs;
- reporting requirements;
- business case.

### Scores

| Criterion                  | Score |
| -------------------------- | ----- |
| Requirements clarification | 10    |
| Impact on architecture     | 8     |
| Risk identification        | 8     |
| Practical value            | 10    |

---

## 23. What happens outside email today?

### Question

How often do support conversations continue through other channels such as website chat, WhatsApp, LinkedIn, forums, or phone calls?

### Why

Email may not be the complete support workflow.

### Impact

Defines:

- future integration opportunities;
- omnichannel requirements;
- roadmap planning.

### Scores

| Criterion                  | Score |
| -------------------------- | ----- |
| Requirements clarification | 9     |
| Impact on architecture     | 9     |
| Risk identification        | 8     |
| Practical value            | 9     |

---

## 24. Which support requests create the highest business risk?

### Question

Which inquiry types create the greatest potential impact if answered incorrectly?

Examples:

- instrument damage;
- calibration errors;
- scientific measurement errors;
- safety concerns;
- warranty claims.

### Why

Not all mistakes have the same consequences.

### Impact

Defines:

- risk-based routing;
- review policies;
- confidence thresholds.

### Scores

| Criterion                  | Score |
| -------------------------- | ----- |
| Requirements clarification | 10    |
| Impact on architecture     | 10    |
| Risk identification        | 10    |
| Practical value            | 10    |

### Example Answer

## Questions related to calibration, measurement accuracy, optical alignment, and hardware modifications. A wrong recommendation can lead to incorrect scientific results or damage to the instrument.

## 25. If the AI could automate only one task during Phase 1, which task would you choose?

### Question

What single activity would save you the most time immediately?

### Why

This forces prioritization and helps define a realistic MVP.

### Impact

Defines:

- MVP scope;
- delivery priorities;
- implementation roadmap.

### Scores

| Criterion                  | Score |
| -------------------------- | ----- |
| Requirements clarification | 10    |
| Impact on architecture     | 9     |
| Risk identification        | 8     |
| Practical value            | 10    |
