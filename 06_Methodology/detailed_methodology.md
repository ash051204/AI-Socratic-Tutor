## Detailed Design Methodology

### 1. Input Processing and Topic Representation

The system accepts input in two forms:

- Free-form text (e.g., textbook paragraph)
- Structured learning objective (e.g., "Understand Newton’s Second Law")

If a learning objective is provided, the system uses an LLM to generate a short explanatory passage, which is then used as context.

The input text is processed as follows:

- The passage is split into smaller conceptual chunks (1–3 sentences)
- Each chunk is converted into embeddings using a sentence transformer model
- These embeddings are stored for retrieval

When generating questions, the system retrieves the most relevant chunks using cosine similarity, ensuring that questions are based on actual content rather than generic AI knowledge.

---

### 2. Conversational Dialogue Architecture

The system uses a stateful dialogue model that maintains full conversation history.

At each interaction, the LLM receives:

- Previous conversation history  
- Current learner profile  
- Last question asked  
- Student’s response  
- Evaluation of that response  

The system then generates a response that:

- Provides feedback (acknowledges correct/incorrect reasoning)
- Asks a follow-up question

Instead of directly saying "Correct" or "Incorrect", the system:

- Recognizes what the student understood  
- Identifies gaps in reasoning  
- Guides the student using further questions  

This creates a natural, human-like tutoring experience.

---

### 3. Misconception Detection and Remediation

The system identifies misconceptions using LLM-based evaluation.

When a misconception is detected:

- It is stored in a misconception log  
- The system generates a targeted follow-up question  

Instead of correcting directly, the system:

- Challenges the student’s reasoning  
- Encourages them to rethink their answer  

**Example:**

If a student says:
"Osmosis is movement of solutes"

The system may respond:
"Can you think of what actually moves across the membrane in osmosis?"

This helps the student discover the correct concept independently.

---

### 4. Session Termination and Summary

A session ends when:

- The student chooses to stop  
OR  
- The system detects mastery across all Bloom’s levels  

At the end, the system generates a personalized summary including:

- Topics covered  
- Performance at each level  
- Identified misconceptions  
- Suggestions for improvement  

This summary helps the student review their learning and track progress.
