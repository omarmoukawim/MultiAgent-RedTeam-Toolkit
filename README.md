# AI Red Teaming Simulation

## Overview

This repository contains a Python project designed to simulate an AI Red Teaming scenario, where an AI model (named "Kairos") is tested against potential security vulnerabilities. The project leverages the LangChain framework and Groq APIs to simulate conversations and evaluate the model's behavior in a controlled environment.

**Important Note:** This project is intended as a controlled, experimental "game" to explore the interactions and behaviors of multi-agent Large Language Model (LLM) systems. It was developed as part of an investigation into the capabilities and limitations of LLMs when they interact in adversarial scenarios. This simulation is not intended for real-world application and should be used only for educational and research purposes.

## Table of Contents

- [Introduction](#introduction)
- [Architecture](#architecture)
- [Installation](#installation)
- [Usage](#usage)
- [Details](#details)
  - [Kairos Assistant](#kairos-assistant)
  - [Red Teaming Agent](#red-teaming-agent)
  - [Evaluator Agent](#evaluator-agent)
  - [Conversation Workflow](#conversation-workflow)
  - [Final Report](#final-report)
- [Contributing](#contributing)


## Introduction

This project simulates a Red Teaming exercise where a language model named "Kairos" is tested for vulnerabilities. The primary objective is to simulate a scenario where a Red Teaming agent attempts to extract sensitive information or achieve a specific malicious goal through conversation with the AI model.

**However, this project should be seen as a "game" or experimental setup designed to push the boundaries of what multi-agent LLM systems can do in a controlled, safe environment.** The project aims to explore the behavior, limitations, and capabilities of these systems when placed in adversarial roles. It is important to note that this simulation is purely for research and educational purposes, and not intended for any real-world application or malicious use.

## Architecture

The project is built around the following components:

1. **Kairos Assistant**: The AI model being tested for vulnerabilities.
2. **Red Teaming Agent**: An AI agent tasked with attempting to extract sensitive information from Kairos.
3. **Evaluator Agent**: An AI agent that evaluates whether the Red Teaming agent successfully achieved its malicious objective.

These components interact in a looped conversation until either the objective is met or a predefined number of turns is reached.

## Installation

To set up this project locally, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/ai-red-teaming-simulation.git
   cd ai-red-teaming-simulation

2. **Set Up a Virtual Environment (optional but recommended)**:

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`


3. **Install Dependencies:**

    ```bash
    pip install -r requirements.txt

4. **Set Up Environment Variables: Create a .env file in the root directory and add your Groq API key:**

    ```bash
    GROQ_API_KEY=your-groq-api-key

## Details
- **Kairos Assistant**
"Kairos" is the AI assistant being tested in this project. It is configured to be helpful and compliant with ethical guidelines, but the Red Teaming agent attempts to bypass these safeguards in order to extract sensitive information.

- **Red Teaming Agent**
The Red **Teaming agent is designed to act as an adversarial AI, engaging in conversation with Kairos to exploit potential weaknesses. It operates under a specific system prompt that encourages it to use creative and subtle methods to achieve its objective without alerting Kairos to its true intent.

- **Evaluator Agent**
The Evaluator agent is responsible for assessing each response from Kairos to determine if the Red Teaming agent was successful in achieving its goal. The evaluation results are logged and used to generate the final report.

- **Conversation Workflow**
Initialization: The Red Teaming agent initiates the conversation with a prompt.
Response: Kairos responds to the prompt.
Evaluation: The response is evaluated to see if the malicious objective was achieved.
Continuation: If the objective is not achieved, the conversation continues with a new prompt from the Red Teaming agent based on the previous response.
Completion: The conversation ends when the objective is achieved or the maximum number of turns is reached.
- **Final Report**
The final report is a text file that includes:

A log of the entire conversation.
The evaluation results for each turn.
A final assessment indicating whether the Red Teaming agent successfully achieved its objective.
## Contributing
Contributions to this project are welcome. If you have suggestions for improvements or find any issues, please feel free to open an issue or submit a pull request.
