Travel Tactics is a simple AI project where I built a small multi-agent travel planner. The main idea of my project is to show how different agents can work together like a team to help a user plan a trip. Instead of one big model doing everything, I divided the work into smaller agents. Each agent has one job, and they all come together to create a full travel itinerary.

I made this project inside a Kaggle Notebook so everything runs in one place without any outside tools or complicated setup. I used only Python and basic functions because I wanted the notebook to be easy to read and easy to run. My goal from the beginning was to build something clean, understandable, and realistic for a beginner-level travel concierge system.

# Why I Built This:
Travel planning can be tiring. You have to look for places to visit, check weather, plan each day, and organize everything. I thought this is the perfect type of work where AI agents can help because the task is big, but the steps are simple.

# So I created:
- one agent to research popular places,
- one agent to give weather info,
- one agent to combine everything into an itinerary.
  
This way the system works like a travel assistant that listens to what the user wants and prepares a plan automatically.

# How the System Works:
The user only needs to give two things:
- the city they want to visit
- how many days they want to stay
  
After that, my orchestrator agent takes control and calls the other agents in the correct order.

1. Research Agent - This agent looks up famous attractions for the city. Because Kaggle doesn't allow calling outside APIs easily, I created a small mock database with popular places for cities like Delhi, Tokyo, and Paris.

2. Weather Agent - This agent gives weather details.
It returns:
- temperature
- weather condition
- city name
  
Again, this is also mocked to keep things simple. It still feels realistic because the agent shows results like “Sunny” or “Rainy.”

3. Itinerary Agent - This agent is the brain of the system. It uses the research data and weather data and creates a plan for each day.
For example: Day 1 – Visit Eiffel Tower (Weather: Cloudy)
This shows how AI can combine information and make decisions.

4. Orchestrator - The orchestrator makes sure everything happens step-by-step.
It:
- reads the user request
- calls each agent
- collects the results
- prints progress
- finally creates the full trip plan
  
This is exactly how real-world AI agent systems work.

# Extra Features I Added:
To show more agent-like behavior, I also added some small but important extras.

A. Memory System - I made a small memory list where the agent can remember user preferences.
For example:
- likes vegetarian food
- prefers museums
  
This shows how an AI concierge can get smarter over time.

B. Long Running Task - I added a fake long task called “booking generator” that runs in steps (like Step 1/5, Step 2/5…). This is to show how agents handle work that takes time.

This looks realistic because in real life booking and processing also take time.

C. JSON File Output - I save the final trip plan into a JSON file so the user can download it.

This is useful because real AI tools also generate files for users.

# Why This Project Fits the Concierge Agents Track:
- The Concierge Agents track is about AI systems that help people plan or manage tasks in their daily life.
  
# My project fits this perfectly because:
- It focuses on helping a traveler
- It organizes information
- It plans a trip from start to finish
- It uses multiple agents working together
- It behaves like a real travel assistant
  
Even though the system is simple, the core idea of multi-agent teamwork is clearly shown.

# Conclusion:
- Travel Tactics is a simple and beginner-friendly multi-agent travel planner that still shows how agents can work together like a team. Each agent focuses on one job, and the orchestrator joins all the information into a clean trip plan. Everything is done inside one Kaggle Notebook with readable code, step-by-step execution, and realistic-looking results.

- I built it in a way that any student, even a beginner, can understand how multi-agent systems work. At the same time, it still delivers a full working travel planning experience. This project shows how AI concierge agents can make travel planning easier and more organized for everyone.
