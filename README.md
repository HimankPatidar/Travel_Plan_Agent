# AI-Powered Travel Planner Agent

This repository contains the documentation and details for the **AI-Powered Travel Planner Agent**, a capstone project developed on the IBM watsonx platform. This intelligent agent is designed to simplify the complex process of travel planning by generating personalized, day-by-day itineraries based on user requests in natural language.

## Table of Contents
- [Problem Statement](#problem-statement)
- [Proposed Solution](#proposed-solution)
- [Demo](#demo)
- [Key Features](#️-key-features)
- [Technology Stack](#️-technology-stack)
- [Architecture](#️-architecture)
- [Development Process](#development-process)
- [Setup and Usage](#️-setup-and-usage)
- [Algorithm & Deployment](#algorithm--deployment)
- [Future Scope](#-future-scope)
- [Conclusion](#-conclusion)
- [License](#-license)

## Problem Statement

A Travel Planner Agent is an AI-powered assistant that helps users plan trips efficiently and intelligently. It uses real-time data to suggest destinations, build itineraries, and recommend transport and accommodation options. By understanding user preferences, budgets, and constraints, it tailors personalized travel plans. Integrated with maps, weather updates, and local guides, it ensures a smooth travel experience. The agent can also manage bookings, alert users to changes, and optimize schedules on the go. This smart assistant transforms complex travel planning into a seamless, enjoyable process.

## Proposed Solution

The proposed solution is an intelligent AI agent named "Plan your Trip," built to simplify travel planning:

- **Intelligent Itinerary Generation**: The agent generates detailed day-by-day travel itineraries based on user needs.
- **Personalization**: It understands and adapts to user preferences and constraints, such as planning a trip that avoids specific types of locations like temples.
- **Conversational Interface**: The system provides a simple chat interface where users can type requests and receive detailed plans, transforming complex planning into a conversation.
- **Personalized trip suggestions** (destinations, activities)
- **Smart itinerary builder** (day-by-day plan)
- **Real-time weather and event alerts**
- **In-app booking and updates**
- **Local insights and cultural tips**

## Demo

The agent successfully handles various requests, from simple trips to complex, multi-city journeys with specific constraints.

| | |
| :---: | :---: |
| *Planning a 15-day trip across the United Kingdom* | *Handling constraints (e.g., "no temples") for a Delhi trip* |
| ![UK Trip Plan](img/Screenshot%202025-08-03%20234130.png) | ![Delhi Trip Plan](img/Screenshot%202025-08-03%20234149.png) |
| *Generating a 4-day itinerary for Jaipur* | *Successful deployment of the agent on IBM watsonx* |
| ![Jaipur Trip Plan](img/Screenshot%202025-08-03%20234917.png) | ![Agent Deployment](img/Screenshot%202025-08-03%20234927.png) |

Additional screenshots showing the agent in action:
- ![Screenshot 1](img/Screenshot%202025-08-03%20234936.png)
- ![Screenshot 2](img/Screenshot%202025-08-04%20000145.png)
- ![Screenshot 3](img/Screenshot%202025-08-04%20001104.png)
- ![Screenshot 4](img/Screenshot%202025-08-04%20001225.png)
- ![Screenshot 5](img/Screenshot%202025-08-04%20002104.png)

## ✨ Key Features

* **Dynamic Itinerary Generation**: Creates detailed, day-by-day travel plans from a single user prompt.
* **Personalized Planning**: Adapts to user preferences and constraints, such as excluding certain types of attractions.
* **Multi-Day & Multi-City Support**: Capable of planning complex, long-duration trips across multiple cities.
* **Conversational Interface**: Users interact with the agent through an intuitive chat interface for a seamless planning experience.

## 🛠️ Technology Stack

The agent is built entirely on the IBM Cloud platform, leveraging state-of-the-art AI services.

* **Cloud Platform**: **IBM watsonx**
* **Foundation Models**: **`llama-3-3-70b-instruct`** and **`mistral-large`** were used as the core language models.
* **Agent Framework**: **LangGraph** was used to structure the agent's logic and manage its conversational state.
* **Core Algorithm**: The agent implements a **ReAct (Reasoning and Acting)** architecture, allowing it to break down complex requests into a series of thought and action steps.
* **External API Integration**:
  * Real-time weather updates
  * Location recommendation services
  * Hotel and transportation booking platforms

## ⚙️ Architecture

The agent uses the **ReAct** architecture. When a user sends a request, the agent doesn't just generate a response. Instead, it enters a loop:

1.  **Thought**: The LLM thinks about the user's request and what steps are needed to fulfill it.
2.  **Action**: It performs an action, such as outlining the plan for the first day.
3.  **Observation**: It observes the outcome of its action and uses this information to plan the next thought and action.

This cycle continues until the entire travel plan is generated, ensuring a logical, coherent, and detailed itinerary.

## Development Process

The development of the AI-Powered Travel Planner Agent followed these key steps:

1. **Problem Identification**: Identified the complexity and time-consuming nature of travel planning as a key problem for travelers.

2. **Technology Selection**: 
   - Chose IBM watsonx platform for agent orchestration and deployment
   - Selected IBM Cloud Lite services for scalable, secure hosting
   - Selected Mistral Large Language Model for its advanced capabilities in understanding natural language and generating personalized itineraries

3. **System Design**:
   - Designed a conversational interface for user interaction
   - Planned integration with external APIs for real-time data
   - Designed the system to handle user preferences, budgets, and constraints

4. **Algorithm Implementation**:
   - Implemented the core functionality using the Mistral Large Language Model
   - Utilized pre-trained model capabilities without custom training
   - Used prompt engineering, retrieval augmented generation (RAG), and API integration for task-specific behavior
   - Implemented feedback loops for performance enhancement

5. **Deployment**:
   - Deployed the agent on the IBM watsonx platform
   - Configured API integrations for real-time data
   - Set up the web-based dashboard or chat UI

6. **Testing**:
   - Tested with various travel scenarios including simple trips and complex multi-city journeys
   - Validated personalization features with constraint-based planning
   - Verified real-time data integration and itinerary generation

7. **Optimization**:
   - Analyzed user satisfaction and retention to optimize prompt formulation
   - Refined workflow design based on testing feedback

## 🚀 Setup and Usage

This project was built and deployed within the IBM watsonx cloud environment. To replicate this agent, follow these steps:

1.  **Create an IBM Cloud Account**: Sign up for a free or paid account on IBM Cloud.
2.  **Navigate to watsonx**: From your IBM Cloud dashboard, access the watsonx.ai platform.
3.  **Build a New Agent**: Go to the Agent Lab (or a similar "build your own agent" studio).
4.  **Configure the Agent**:
    * Set the **Framework** to `LangGraph`.
    * Set the **Architecture** to `ReAct`.
    * Choose a foundational **Model** like `llama-3-3-70b-instruct` or `mistral-large`.
5.  **Set Instructions**: In the instructions panel, provide the guiding prompt for the agent. Use the following text from the project:
    > `You are an intelligent agent who plans trip according to user's needs. Consider the weather and places to visit in city. Generate a detailed itinerary day-by-day, considering realistic travel time, local culture, and weather. Keep suggestions practical and enjoyable`.
6.  **Deploy**: Save and deploy the agent within the watsonx platform.
7.  **Test**: Use the "Preview" or "Test" chat panel to interact with your newly created travel agent.

## Algorithm & Deployment

### Algorithm Selection

The core of the Travel Planner Agent is powered by the Mistral Large Language Model (LLM), selected for its advanced capabilities in understanding natural language, multi-turn reasoning, and generating personalized, actionable itineraries. Mistral was chosen because it excels at interpreting user input, integrating external data sources, and dynamically constructing day-by-day travel plans tailored to user preferences and real-time conditions.

### Data Input

The agent utilizes the following inputs:
- User preferences: desired destination, travel dates, budget, personal interests (sightseeing, food, adventure, relaxation, etc.)
- Real-time data: weather forecasts, local events, COVID advisories, transportation availability, hotel and activity options (via API integrations)

### Training Process

The Mistral model is pre-trained on massive datasets for language understanding and reasoning, eliminating the need for custom model training. Task-specific behavior (trip planning and information retrieval) is achieved through prompt engineering, retrieval augmented generation (RAG), and integration with APIs for up-to-date information. If required, performance is enhanced using feedback loops—analyzing user satisfaction and retention to optimize prompt formulation and workflow design.

### Prediction Process

Upon receiving user input, the agent parses preferences and retrieves relevant real-time data from integrated APIs. The Mistral model uses this information, along with internal logic (ReAct/LangGraph), to generate a detailed, practical itinerary. The output includes optimized day-wise plans, personalized recommendations, and real-time updates (such as weather-based activity suggestions or alerts about closures). Results are delivered instantly through a chat or web interface, with continuous updating capabilities as the user interacts or as external conditions change.

## 🔮 Future Scope

Based on the project plan, potential enhancements include:

* **API Integration**: Connect the agent to real-time APIs for booking flights and hotels.
* **Knowledge Base Enhancement**: Add a vector index with travel guides or user reviews to provide richer suggestions.
* **Custom Tool Creation**: Develop specific tools for tasks like currency conversion or budget calculation.
* **Standalone Application**: Deploy the agent as a standalone web or mobile application for broader access.
* **Enhanced Real-time Data**: Integrate more real-time data sources such as live traffic, public transport schedules, and user reviews to offer richer, personalized itineraries.
* **Multimodal Travel Planning**: Expanding coverage to multiple cities and enabling multimodal travel planning can broaden its usability.
* **Advanced User Preference Learning**: Leveraging advanced learning of user preferences can enable tailored recommendations over time.
* **Edge Computing and Blockchain**: Leveraging edge computing and blockchain for faster, secure transactions will boost performance and trustworthiness.

## 📄 Conclusion

The AI-powered Travel Planner Agent successfully addresses the complexity and challenges of personalized trip planning by leveraging advanced Large Language Models, specifically the Mistral model, deployed on IBM Cloud Lite. The system intelligently generates detailed, day-by-day itineraries that consider user preferences, real-time weather updates, local culture, and practical travel constraints.

By integrating dynamic data sources and utilizing sophisticated prompt engineering and orchestration techniques (LangGraph and ReAct), the agent provides users with seamless, adaptive travel experiences. Its ability to handle multi-turn conversations and update itineraries on the fly enhances user satisfaction and reduces planning time significantly.

Despite challenges associated with real-time data integration and contextual understanding, the solution demonstrates a robust, scalable approach to travel planning utilizing cutting-edge AI and cloud technologies. The Travel Planner Agent proves its potential as a valuable tool for travelers seeking efficient, enjoyable, and personalized trip arrangements.

## 📄 License

This project is licensed under the MIT License.
