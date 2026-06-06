### 1. Logical Context Decomposition | UML | PlantUML

This diagram shows the main logical business contexts of the AI Customer Inquiry Management System.

//www.plantuml.com/plantuml/png/ZLH1Rziy3BthLn0fyDtQRqtYDBqCJPscAxPYG8jjbrqucqc4sf8hKMspeVzzj2EdZhC1EmZG4zyZ-Kp95vxHSIWBnPeBWazsfJCi8BM6wOLXhd7biFnkPZUG1i-s90StvZ5eju5RDBYYaWp3_SOpbKhv1sqg50LKc3r8z9utajPHncXM1NK8mLE6dk2N0hWKyihPOFBK5jR1jxLcgi-joybjpux6ioIPJDMhKfYnTRj-8XnS1gyDUG-Vdmqv-1_kRwy6W14hjMi21l_aPY2jAOX6H7Hw8jpCbjgi_Y0QmD5ySZLRJ1j3qDgJMWQBpKy2tMhrLjkqzYKztMUd1Nglbnj0aqFbj7MQjQWTFGRo74N3VT6T3KnjNc0BQr4NTQqAUHqr8z6yxXaQdi17OvyBoWNz1tV4JjCJ5ZrNoIAv6lLTHJA13rLb7KlrfNKbihOc5Xp_HP75Bt_iAyhqKcT2zyG-of9zsLSiT8vYpqLz3jdsSaR-vC3Nw4Iy-CeQJnqhul13AD58x4dJipXRf8jHkkWxkoP3hYwOErmok9WfLZlhcsh60kiciukP6-QqTmsgojcE-txYymCRu-vuhaNh39fC9jMyJcs23HvkoYPjdDLYDh-S7zn0UTITCR6uopfZEdtNku5OSN04k6qu1tgfI9GFRI-jhdTpRr5ooteZmW_qE_QmyISETm_l-FXz7UWVd2ibfn4CbQou7zM1KGJZpZwf0-C89h9FTdi1amZEbAoudwhjFw95ihhL8qq-pIuImVaRs4iX7wC-t4Ej1x5-GIOFPV4R

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

### 5. 2. Retrieval Strategy Sequence Diagram

Цель: показать, как система выбирает источник данных.

Логика:

If exact order/customer data is needed → Operational Data Sources

If customer-specific file is needed → Support Asset Repository

If explanation/recommendation/troubleshooting is needed → RAG Knowledge Base

Эта диаграмма отвечает на вопрос:

How does the system decide where to retrieve information from?
