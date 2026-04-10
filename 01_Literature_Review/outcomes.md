## Outcome of Literature Review

A careful analysis of the reviewed papers reveals several important patterns in the field of AI-based question generation and tutoring systems.

First, the technical quality of automatic question generation has improved significantly in recent years. The shift from rule-based and template-based methods to transformer-based models has led to better fluency, relevance, and contextual understanding. Modern models like T5 and GPT can generate grammatically correct and meaningful questions from educational content.

However, the pedagogical quality of these questions has not improved at the same pace. Most systems are evaluated using metrics such as BLEU, ROUGE, and METEOR, which measure similarity to existing questions but do not evaluate whether the question is actually useful for learning. As a result, many generated questions may be correct but still lack depth or educational value.

Another major limitation is that most question generation systems operate independently. They generate questions from text but do not engage in a continuous interaction with the student. There is no follow-up questioning, no dialogue, and no step-by-step guidance, which are essential for deeper understanding.

Additionally, adaptive learning is largely missing in existing systems. While some research discusses difficulty levels, very few systems adjust question difficulty dynamically based on student responses. This lack of real-time adaptation makes it difficult to personalize learning.

Finally, none of the reviewed papers presents a complete Socratic tutoring system. Although some works mention the importance of guided questioning, there is no system that fully implements a continuous dialogue where the AI asks questions, understands responses, identifies misconceptions, and guides the student step-by-step.

---

### Key Insight

Overall, current research improves question generation, but lacks integration of:
- Socratic questioning
- Adaptive learning
- Conversational interaction

This clearly highlights the need for a unified system that combines all three.
