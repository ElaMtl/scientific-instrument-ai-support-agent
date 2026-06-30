### 1. Logical Component-Context Diagram | UML | PlantUML

This diagram shows the main logical business contexts of the AI Customer Inquiry Management System.

@startuml
title Logical Component Context Diagram\nAI Customer Inquiry Management System

skinparam componentStyle rectangle

actor Customer
actor "Business Owner / SME" as Owner

rectangle "AI Customer Inquiry Management System" {

component "Incoming Inquiry\nManagement" as IIM #D6EAF8
note right of IIM - Analyze incoming inquiry - Classify and prioritize request - Route inquiry to handling path
end note

component "Knowledge & Retrieval\nManagement" as KRM #D5F5E3
note right of KRM - Retrieve support information - Retrieve customer-specific assets - Validate retrieved context
end note

component "Response Management\n& Human Review" as RMHR #FCF3CF
note right of RMHR - Generate draft response - Request human review - Approve customer response
end note

component "Knowledge Governance\n& Continuous Improvement" as KGCI #FADBD8
note right of KGCI - Log support interaction - Capture approved expert knowledge - Maintain knowledge base
end note
}

Customer --> IIM : sends inquiry
IIM --> KRM : routes request
KRM --> RMHR : provides retrieved context
RMHR --> Owner : requests review if needed
Owner --> RMHR : approves / corrects response
RMHR --> KGCI : logs resolved case
Owner --> KGCI : contributes expert knowledge
KGCI --> KRM : updates knowledge sources

@enduml

### 2. Customer Inquiry Handling (AS-IS) | BPMN | Storm

### 3. AI Customer Inquiry Management Agent (TO-BE) | BPMN | Storm

### 4. The diagram below shows the MVP classification and routing logic for incoming company emails. The workflow is routed by one primary category and one primary next action. Multi-intent email processing is excluded from the MVP scope and considered a future enhancement.

### 4. High-Level Email Processing Sequence Diagram

Цель: показать всю архитектуру обработки входящего email.

Компоненты:

Customer
Email Inbox
Classification & Routing Model
Retrieval Router
Operational Data Sources
Support Asset Repository
RAG Knowledge Base
Draft Response Model
Business Owner
Processing Log

Эта диаграмма отвечает на вопрос:

What happens when a new email arrives?

Именно её нужно делать первой.

### 5. Retrieval Strategy Sequence Diagram

Цель: показать, как система выбирает источник данных.

Логика:

If exact order/customer data is needed → Operational Data Sources

If customer-specific file is needed → Support Asset Repository

If explanation/recommendation/troubleshooting is needed → RAG Knowledge Base

Эта диаграмма отвечает на вопрос:

How does the system decide where to retrieve information from?
