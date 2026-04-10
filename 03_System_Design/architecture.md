## System Architecture

The overall architecture of the AI Teaching Assistant is designed as a pipeline with feedback loops. Unlike traditional question-answer systems that treat each interaction separately, this system maintains context throughout the entire session and uses previous interactions to guide future responses.

### Key Components

The system consists of the following five main components:

- **Topic Ingestion Layer**  
  This component accepts input in the form of text passages, textbook content, or learning objectives. It processes the input by tokenizing, chunking, and converting it into embeddings to create a semantic representation for further use.

- **Question Generation Module**  
  This module generates questions based on the input content and the learner’s current level. It uses a large language model (LLM) with structured prompts aligned to Bloom's Taxonomy to produce questions of appropriate difficulty and type.

- **Dialogue Manager**  
  This component maintains the entire conversation history. It ensures that each new response is context-aware by combining the student’s input, previous questions, and the learner profile.

- **Learner Response Evaluator**  
  This module evaluates the student’s answer by checking correctness and reasoning quality. It uses semantic similarity techniques and LLM-based evaluation to identify understanding or misconceptions.

- **Adaptive Difficulty Controller**  
  This component tracks student performance over time and adjusts the difficulty level of questions. It increases complexity when the student performs well and reduces it when the student struggles.

---

### Working of the System

1. The student starts by entering a topic or providing learning material.
2. The Topic Ingestion Layer processes the input and prepares it for question generation.
3. The system generates an initial question at the basic (recall) level to assess the student’s knowledge.
4. The student responds to the question.
5. The Learner Response Evaluator analyzes the answer and assigns a performance score.
6. The Dialogue Manager uses this information to generate a follow-up response.
7. The Adaptive Difficulty Controller updates the learner profile and decides the next question level.
8. This process continues in a loop, gradually increasing or decreasing difficulty based on performance.
9. The session ends when the student achieves mastery or chooses to stop.

---

### Key Feature

The system continuously adapts to the student’s understanding and maintains a guided conversational flow, making learning interactive, personalized, and concept-driven.
