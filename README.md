# AI-Powered Travel Planner Agent

[cite_start]This repository contains the documentation and details for the **AI-Powered Travel Planner Agent**, a capstone project developed on the IBM watsonx platform[cite: 1, 2]. [cite_start]This intelligent agent is designed to simplify the complex process of travel planning by generating personalized, day-by-day itineraries based on user requests in natural language[cite: 1, 2, 3].

## Demo

The agent successfully handles various requests, from simple trips to complex, multi-city journeys with specific constraints.

| | |
| :---: | :---: |
| [cite_start]*Planning a 15-day trip across the United Kingdom* [cite: 3] | [cite_start]*Handling constraints (e.g., "no temples") for a Delhi trip* [cite: 2] |
| ![UK Trip Plan](http://googleusercontent.com/file_content/3) | ![Delhi Trip Plan](http://googleusercontent.com/file_content/2) |
| [cite_start]*Generating a 4-day itinerary for Jaipur* [cite: 1] | *Successful deployment of the agent on IBM watsonx* |
| ![Jaipur Trip Plan](http://googleusercontent.com/file_content/1) | ![Agent Deployment](http://googleusercontent.com/file_content/0) |

## ✨ Key Features

* [cite_start]**Dynamic Itinerary Generation**: Creates detailed, day-by-day travel plans from a single user prompt[cite: 1, 3].
* [cite_start]**Personalized Planning**: Adapts to user preferences and constraints, such as excluding certain types of attractions[cite: 2].
* [cite_start]**Multi-Day & Multi-City Support**: Capable of planning complex, long-duration trips across multiple cities[cite: 3].
* [cite_start]**Conversational Interface**: Users interact with the agent through an intuitive chat interface for a seamless planning experience[cite: 3].

## 🛠️ Technology Stack

The agent is built entirely on the IBM Cloud platform, leveraging state-of-the-art AI services.

* [cite_start]**Cloud Platform**: **IBM watsonx**[cite: 1].
* [cite_start]**Foundation Models**: **`llama-3-3-70b-instruct`** and **`mistral-large`** were used as the core language models[cite: 1, 2].
* [cite_start]**Agent Framework**: **LangGraph** was used to structure the agent's logic and manage its conversational state[cite: 1, 2].
* [cite_start]**Core Algorithm**: The agent implements a **ReAct (Reasoning and Acting)** architecture, allowing it to break down complex requests into a series of thought and action steps[cite: 1, 2].

## ⚙️ Architecture

The agent uses the **ReAct** architecture. When a user sends a request, the agent doesn't just generate a response. Instead, it enters a loop:

1.  **Thought**: The LLM thinks about the user's request and what steps are needed to fulfill it.
2.  **Action**: It performs an action, such as outlining the plan for the first day.
3.  **Observation**: It observes the outcome of its action and uses this information to plan the next thought and action.

This cycle continues until the entire travel plan is generated, ensuring a logical, coherent, and detailed itinerary.

## 🚀 Setup and Usage

This project was built and deployed within the IBM watsonx cloud environment. To replicate this agent, follow these steps:

1.  **Create an IBM Cloud Account**: Sign up for a free or paid account on IBM Cloud.
2.  **Navigate to watsonx**: From your IBM Cloud dashboard, access the watsonx.ai platform.
3.  **Build a New Agent**: Go to the Agent Lab (or a similar "build your own agent" studio).
4.  **Configure the Agent**:
    * [cite_start]Set the **Framework** to `LangGraph`[cite: 1, 2].
    * [cite_start]Set the **Architecture** to `ReAct`[cite: 1, 2].
    * [cite_start]Choose a foundational **Model** like `llama-3-3-70b-instruct`[cite: 2].
5.  **Set Instructions**: In the instructions panel, provide the guiding prompt for the agent. Use the following text from the project:
    > `You are an intelligent agent who plans trip according to user's needs. Consider the weather and places to visit in city. Generate a detailed itinerary day-by-day, considering realistic travel time, local culture, and weather. [cite_start]Keep suggestions practical and enjoyable`[cite: 1, 2].
6.  **Deploy**: Save and deploy the agent within the watsonx platform.
7.  [cite_start]**Test**: Use the "Preview" or "Test" chat panel to interact with your newly created travel agent[cite: 3].

## 🔮 Future Scope

[cite_start]Based on the project plan, potential enhancements include[cite: 4]:

* **API Integration**: Connect the agent to real-time APIs for booking flights and hotels.
* [cite_start]**Knowledge Base Enhancement**: Add a vector index with travel guides or user reviews to provide richer suggestions[cite: 4].
* **Custom Tool Creation**: Develop specific tools for tasks like currency conversion or budget calculation.
* [cite_start]**Standalone Application**: Deploy the agent as a standalone web or mobile application for broader access[cite: 4].

## 📄 License

This project is licensed under the MIT License.
