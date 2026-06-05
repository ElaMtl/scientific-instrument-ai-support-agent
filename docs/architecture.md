#

## Architecture Decision: Retrieval-First Support Automation

The MVP follows a retrieval-first approach.

Before generating a response, the workflow searches existing sources of truth in the following order:

1. Sent Email Archive
2. External Order Register
3. Knowledge Base

This design reduces hallucination risk and allows the AI workflow to reuse already verified customer-specific information such as calibration files, licenses, drivers, shipment details, and onboarding materials.

The MVP does not create a new CRM or duplicate operational data. It uses existing data sources and stores only workflow-level outputs such as classification results, lookup results, draft responses, logs, and human review decisions.
