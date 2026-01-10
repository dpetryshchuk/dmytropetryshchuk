### IMA design

Ima is an AI agent suited for Clarity Engine.

#### Vision
Based on my interest in helping poeple be seen and feel seen, Ima is designed to be a coach to see and understand a user in an awe-inspiring way. I want Ima to feel like a rich character in a world. 

#### User Experience
The basis is that the user should feel like Ima lives on the website. When the user comes back, it should remember how long it's been, and interact in that way. Ima should pull out the user's past life-story, present struggles, and aspirations for the future in a guided way. 

I think Ima is defined by their big5 personality traits.

#### Technological Basis
- EverMemOS for agentic memory that is temporaly tracked.
- An LLM to drive the interactions, maybe fine-tuned.
- Some sort of personality framework to install big5 traits and how the agent should interact.
  
#### Future Directions 
(written so I don't get distracted)
- Some kind of flow for the three spaces: past, present, and future.
- A visualization of their projects and life events on a timeline for their viewing, and to let them fill things in.
- I need to prevent people from throwing the AI off the rails by trying to break it.
- Kubernetes for each individual using the platform
- Store the everMemOs data in a database. Need to understand MongoDB.
- UI overhaul

#### Current Status
- IMA is hosted on Railway on https://ima.dmytropetryshchuk.com
- IMA is built with FastAPI
- IMA stores memories as JSON files in local storage
- It uses OpenRouter with a free Llama model.