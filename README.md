# ✈️ Travel Multi Agent (BeeAI Framework)
A sophisticated travel planning application built using the BeeAI Framework. This project orchestrates multiple autonomous AI agents—each with a specific role (Destination Expert, Travel Meterologist, Cultural and Language expert)—to collaborate with a Travel Coordinater AI agent and generate detailed, constraint-aware travel itineraries for users

## 📖 Table of Contents
- Key Features

- How It Works

- Project Structure

- Prerequisites

- Installation

- Configuration

- Usage

- Future Roadmap

## 🌟 Key Features
- Multi-Agent Orchestration: Uses the BeeAI Framework's workflow engine to manage state and handoffs between different agents.

- Real-Time Data: Integrated with tools like DuckDuckGoTool, OpenMeteroTool and WikipediaTool, to fetch up-to-date flight prices, weather, and local culture and events.

- Constraint Validation: A dedicated Budget Agent ensures the proposed itinerary adheres to the user's financial limits.

- Memory Management: Agents maintain context throughout the planning process to ensure preferences (dietary, accessibility, budget, etc.) are respected in every step.

- Structured Output: Generates the final plan in a clean JSON format.

## ⚙️ How It Works
This system utilizes a Sequential Workflow pattern where agents pass the "Travel Plan State" to one another.

- User Input: The user provides a prompt (e.g., "Plan a 5-day trip to Tokyo for $2000").

- Travel Coordinater Agent: Analyzing the prompt to extract variables: Destination, Dates, Budget, Interests.

- Destination Agent: Uses Wikipedia tool and Think tool to think and find Top attractions matching interests.

- - Flight options.

- - Hotel availability.
 
- Meterologist Agent: Uses Weather tools like OpenMeteroTool() to retrive weather information of the location


- Language and culture Agent: Uses Wikipedia tool to retrive information about the languages they speak and the culture people have in the location, to help the user to have an better experience. 

- Final Output: A complete itinerary is presented to the user.
