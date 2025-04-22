# 🧠 AI-Powered Customer Support Agent using Salesforce Einstein

This project showcases a smart, AI-powered customer support chatbot built using **Salesforce Einstein** and **Agentforce**. It was developed during a hands-on workshop hosted by **GeeksforGeeks** on April 20, 2024. The agent simulates guest support for a fictional resort — Coral Cloud Resorts — and demonstrates how AI, automation, and custom logic can enhance customer service.

> 💡 This is a no-code/low-code AI project, ideal for professionals looking to bridge the gap between data science, AI tools, and enterprise solutions.

---

## 🔧 Features Implemented

- 💬 **Customer Experience Support Agent**
  - Helps guests find and book resort experiences.
  - Handles queries like event details (e.g. Full Moon Beach Party).

- ⚙️ **Custom Actions using Flow**
  - `Get Experience Details`: Retrieves activity descriptions.
  - `Issue Resort Credit`: Issues resort credits to specific contacts.

- 🧑‍💻 **Apex-Driven Actions**
  - `CheckWeather`: Invokes a weather API and provides forecasts based on user-provided dates.

- 🤖 **Conversational AI Integration**
  - Uses topics, prompt templates, and a reasoning engine to guide user interactions.
  - Built with Einstein Copilot and Agentforce Studio.

---

User: Can you let me know more about the full moon beach party experience?
Bot: The Full Moon Beach Party includes bonfire, music, and beach games...

User: Issue $100 resort credit to contact named Sofia Rodriguez
Bot: Resort credit of $100 has been issued to Sofia Rodriguez. ID: CRD-03491

User: Check the weather for tomorrow
Bot: Temperatures will be between 22°C (71°F) and 30°C (86°F) at Coral Cloud Resorts.




## 🧱 Architecture Overview

```mermaid
graph TD;
    User["Customer"]
    Chatbot["Einstein Agent"]
    Flow["Custom Flow Actions"]
    Apex["Apex Class: CheckWeather"]
    SalesforceDB["Salesforce CRM Data"]

    User --> Chatbot
    Chatbot --> Flow
    Chatbot --> Apex
    Flow --> SalesforceDB
    Apex --> ExternalAPI["Weather API"]

