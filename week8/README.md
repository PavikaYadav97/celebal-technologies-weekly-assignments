# Week 8: Single Agent Smart Assistant using Agentic AI

## Overview

This project demonstrates the implementation of a simple Single-Agent AI system capable of understanding user queries, routing them based on intent, invoking appropriate tools, and returning structured JSON responses. The project introduces the core concepts of Agentic AI, including conditional routing, tool integration, and basic error handling.

---

## Objective

To build a Single-Agent Smart Assistant that:

- Understands user queries.
- Routes tasks based on user intent.
- Uses appropriate tools to process requests.
- Returns structured JSON responses.
- Demonstrates the basic workflow of an Agentic AI system.

---

## Features

- Rule-based intent detection.
- Mathematical calculations using a Calculator Tool.
- Keyword extraction from text.
- General response handling.
- Structured JSON output.
- Basic error handling for invalid calculations.

---

## Tools Used

### Calculator Tool
Evaluates mathematical expressions entered by the user and returns the computed result.

### Keyword Extraction Tool
Extracts important keywords from input text by selecting unique words with more than four characters.

---

## Agent Workflow

```
                User Query
                     │
                     ▼
             Intent Detection
                     │
      ┌──────────────┼──────────────┐
      ▼              ▼              ▼
 Calculation     Keyword Tool   General Query
      │              │              │
      └──────────────┼──────────────┘
                     ▼
          Structured JSON Output
```

---

## Technologies Used

- Python
- JSON
- Conditional Routing
- Rule-Based Decision Making

---

## Project Structure

```
Week-8/
│
├── Week8_Assignment.ipynb
└── README.md
```

---

## Sample Queries

### Calculator

```
Calculate 20 + 5
```

Output

```json
{
    "type": "calculation",
    "result": "25"
}
```

---

### Keyword Extraction

```
Extract keywords from Artificial Intelligence is transforming industries
```

Output

```json
{
    "type": "keywords",
    "result": [
        "artificial",
        "intelligence",
        "transforming",
        "industries"
    ]
}
```

---

### General Query

```
What is Machine Learning?
```

Output

```json
{
    "type": "general",
    "result": "Machine Learning is a branch of Artificial Intelligence that enables computers to learn patterns from data and make predictions without being explicitly programmed."
}
```

---

## Learning Outcomes

- Understood the fundamentals of Agentic AI.
- Implemented rule-based intent detection.
- Integrated multiple tools within a single-agent system.
- Learned conditional routing techniques.
- Generated structured JSON responses.
- Implemented basic error handling for reliable execution.

---

## Future Scope

- Integrate an LLM for intelligent intent classification.
- Add conversational memory.
- Support multiple tool invocations in a single query.
- Integrate external APIs such as Weather, Search, and Translation.
- Extend the project into a multi-agent architecture.

---

## Conclusion

This project successfully demonstrates the implementation of a Single-Agent Smart Assistant capable of routing user queries, invoking appropriate tools, and generating structured JSON responses. It provides a strong foundation for understanding Agentic AI systems and can be further enhanced with LLMs, memory, and advanced tool integration.
