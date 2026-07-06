**Author:** Elvina Cherepovich  
**Role:** Technical Business Systems Analyst  
**Project:** AI Customer Inquiry Management Agent  
**Version:** 1.0  
**Last Updated:** 2026-07-05

# Portfolio MVP Scope

## First Selected End-to-End Scenario

The portfolio MVP focuses on one customer support scenario: recovery of a missing calibration file.

A customer contacts the company and requests a previously issued calibration file.

The solution shall:

1. Receive the incoming customer email.
2. Identify the request as a calibration file recovery request.
3. Identify the customer and relevant instrument or order.
4. Retrieve the corresponding calibration file.
5. Validate that the file belongs to the identified customer and instrument.
6. Generate a customer response and attach the retrieved file.
7. Automatically send the response when all validation criteria are satisfied.
8. Route the case to human review when customer identity, instrument matching, or file retrieval is ambiguous or insufficiently reliable.

## Portfolio Scope Principle

The broader AI Customer Inquiry Management Agent is documented as the target solution.

Detailed requirements, design, implementation, and demonstration will focus on the selected calibration file recovery scenario.

Other inquiry types remain outside the implementation scope of the portfolio MVP.

## MVP Decision

The MVP is not limited to draft creation only.

The selected scenario supports straight-through processing when validation is successful and exception-based human review when risk or uncertainty is detected.

## In Scope

- Incoming email processing for calibration file recovery requests.
- Request classification.
- Customer identification.
- Instrument or order identification.
- Calibration file retrieval.
- Customer-to-asset validation.
- Draft response generation.
- Attachment of the retrieved calibration file.
- Automatic email sending for validated cases.
- Human review routing for ambiguous, incomplete, or risky cases.

## Out of Scope

- Full automation of all inquiry types.
- Complex technical consultation.
- Product selection and application guidance.
- Pricing and quotation generation.
- Custom development requests.
- Financial decisions.
- Automatic handling of conflicting customer records.
- Automatic sending when customer identity or file matching is uncertain.
