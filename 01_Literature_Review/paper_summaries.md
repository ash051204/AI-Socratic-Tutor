# Literature Review

The development of an AI Teaching Assistant grounded in the Socratic Method draws on several overlapping fields of research: automatic question generation (AQG), intelligent tutoring systems (ITS), Bloom's Taxonomy-based adaptive learning, and large language model (LLM) applications in education.

This literature review surveys ten significant research contributions across these domains, analyses their comparative strengths and limitations, and identifies the research gap that this project seeks to address.

---

## Detailed Review of Papers

### Paper 1: Automatic Question Generation and Answer Assessment: A Survey (2021)

This survey provides a comprehensive overview of the AQG field up to 2021, covering both traditional rule-based methods and early neural approaches. The authors review question generation from multiple source types, including structured text, reading comprehension passages, and knowledge graphs, along with answer assessment methods.

A key contribution is the classification of question types into factual, conceptual, and procedural. This is important for Socratic learning as it helps structure questioning levels.

However, the paper highlights that most systems focus on factual questions and struggle with higher-order conceptual questioning.

---

### Paper 2: A Survey of Approaches to Automatic Question Generation (2021)

This paper compares rule-based, template-based, and neural approaches. It shows how systems evolved from simple grammar-based transformations to deep learning models.

While neural models perform better, they often generate repetitive or hard-to-control questions. The paper also highlights the lack of difficulty control in existing systems.

---

### Paper 3: Automatic Question Generation: A Review (2023)

This paper focuses on transformer-based models like BERT, T5, and GPT. These models improve fluency and context understanding.

It introduces answer-aware and answer-agnostic question generation. However, it highlights that current evaluation methods do not measure educational effectiveness properly.

---

### Paper 4: Towards Automatic Question Generation Using Pre-trained Language Models (2024)

This paper explores using models like T5 and GPT for generating questions.

It shows that fine-tuned models perform well, but large LLMs can also work effectively using prompt engineering. It also introduces objective-based question generation aligned with learning goals.

---

### Paper 5: Automatic Question-Answer Pair Generation in Education (2024)

This paper generates both questions and answers using a two-step process.

While useful for assessment systems, it mainly works for factual questions and struggles with conceptual reasoning.

---

### Paper 6: A Survey on Neural Question Generation (IJCAI 2024)

This survey categorizes question generation based on input type, output type, and model architecture.

It highlights multi-hop questions, which are important for higher-level thinking, but also notes that integrating question generation with dialogue systems is still a challenge.

---

### Paper 7: Automating Question Generation from Educational Text (2023)

This paper focuses on generating questions from textbooks.

It introduces curriculum-aware question generation, ensuring questions match the learner’s level. However, it lacks real-time interaction with students.

---

### Paper 8: Automatic Question Generation using Machine Learning (2022)

This paper discusses machine learning approaches including traditional ML and deep learning.

It highlights limitations like language dependency and lack of flexibility, but provides a base for difficulty estimation.

---

### Paper 9: Controllable Open-ended Question Generation (2021)

This paper introduces controllable question generation where the system can adjust type and difficulty.

It improves question quality but does not include learner feedback or interaction.

---

### Paper 10: Future of Learning in the Age of Generative AI (2024)

This paper discusses how AI can transform education using personalized learning.

It strongly supports Socratic learning but does not provide an actual implementation.

---

## Summary

From the literature, it is clear that:

- Question generation systems exist but lack interaction
- Conversational systems exist but lack structure
- Adaptive systems exist but are not integrated

This highlights the need for a system that combines Socratic questioning, adaptive learning, and conversational AI.
