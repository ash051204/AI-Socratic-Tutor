## Algorithms and Techniques

### 1. Bloom's Taxonomy-Based Question Level Classification

Bloom's Taxonomy forms the core structure for question generation in this system. It defines six levels of cognitive learning, each corresponding to a different type of question:

- **Level 1 — Remember**  
  Focuses on recalling basic facts and definitions.  
  *Example:* What is the definition of osmosis?

- **Level 2 — Understand**  
  Requires explanation of concepts in one's own words.  
  *Example:* Can you explain what happens to water molecules during osmosis?

- **Level 3 — Apply**  
  Involves using knowledge in new situations.  
  *Example:* If a cell is placed in a highly concentrated salt solution, what would happen and why?

- **Level 4 — Analyse**  
  Requires breaking down concepts and examining relationships.  
  *Example:* What factors determine the direction of osmotic movement?

- **Level 5 — Evaluate**  
  Involves judgement or critical thinking.  
  *Example:* Do you agree that osmosis is simply diffusion of water? Why or why not?

- **Level 6 — Create**  
  Focuses on generating new ideas or solutions.  
  *Example:* Design an experiment to demonstrate osmotic pressure.

#### Progression Strategy

The system begins at Level 1 and adjusts difficulty based on student performance:

- If a student answers **3 consecutive questions correctly (≥70%)**, the level increases.
- If performance drops below **40%**, the level decreases.
- A sliding window approach is used to track performance dynamically.

---

### 2.LLM-Based Question Generation with Structured Prompting

Question generation is implemented using a Large Language Model (LLM) such as GPT-4.

#### Key Idea

Instead of random generation, the system uses **structured prompting** to control:

- Question type  
- Difficulty level (Bloom’s level)  
- Target concept  
- Context (student’s previous answer)

#### Prompt Components

Each prompt includes:

- Topic or learning content  
- Current Bloom's level  
- Target concept  
- Student’s previous response  
- Identified misconceptions  
- Instruction to generate open-ended, non-direct questions  

#### Socratic Persona

A special **persona prompt** is used to ensure:

- No direct answers are given  
- The system always responds with guiding questions  
- Tone remains supportive and thought-provoking  

This ensures the AI behaves like a **Socratic tutor** instead of a normal chatbot.

---

### 3. Semantic Similarity for Response Evaluation

Evaluating student responses is done using a hybrid approach:

#### Step 1: Reference Answer Generation
For each question, the system internally generates a correct reference answer.

#### Step 2: Semantic Similarity
- The student’s answer is compared with the reference answer  
- Uses sentence embeddings (`all-mpnet-base-v2`)  
- Cosine similarity score is calculated (range: 0 to 1)

#### Step 3: LLM-Based Evaluation
- The LLM evaluates:
  - Correctness  
  - Depth of understanding  
  - Misconceptions  

- It provides a rating (1 to 5)

#### Final Scoring

The final score is calculated as a combination of:

- Semantic similarity score  
- LLM evaluation score  

This combined score is used by the system to:

- Update learner performance  
- Adjust difficulty level  
- Identify misconceptions  
