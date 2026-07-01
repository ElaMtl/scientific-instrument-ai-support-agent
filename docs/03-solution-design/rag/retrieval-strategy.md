#

## Architecture Decision: Retrieval-First Support Automation

The MVP follows a retrieval-first approach.

Before generating a response, the workflow searches existing sources of truth in the following order:

1. Sent Email Archive
2. External Order Register
3. Knowledge Base

This design reduces hallucination risk and allows the AI workflow to reuse already verified customer-specific information such as calibration files, licenses, drivers, shipment details, and onboarding materials.

The MVP does not create a new CRM or duplicate operational data. It uses existing data sources and stores only workflow-level outputs such as classification results, lookup results, draft responses, logs, and human review decisions.

### 1. Operational Data Sources (Structured Lookup)

Used to retrieve exact customer and order information.

- Order Register (Google Sheet)
- Customer records
- Serial numbers
- Order status
- Shipment dates
- Tracking numbers
- Sales channel references

---

### 2. Support Asset Repository (File Retrieval)

Used to locate and deliver customer-specific files.

- Calibration files
- Software licenses
- Drivers
- Software packages
- User manuals (PDF)
- Installation guides

---

### 3. RAG Knowledge Base (Semantic Search)

Used to answer questions, provide recommendations, and support troubleshooting.

- Product descriptions
- Product specifications
- FAQ
- Troubleshooting guides
- Application notes
- Product comparison guides
- Technical documentation
- Approved support responses
- Historical support knowledge

---

### Decision Rule

```text
Need exact data? → Operational Data Sources

Need a file? → Support Asset Repository

Need an explanation, recommendation, or troubleshooting guidance? → RAG Knowledge Base
```
