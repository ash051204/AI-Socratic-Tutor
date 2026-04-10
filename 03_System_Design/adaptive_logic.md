### Adaptive Difficulty Control Algorithm

The adaptive difficulty controller is responsible for adjusting the level of questions based on the student’s performance during the session.

#### Learner Profile

The system maintains a learner profile with the following components:

- **Current Bloom's Level** (1 to 6)  
- **Performance Score** (rolling average of recent responses)  
- **Misconception Log** (records incorrect concepts identified)  
- **Coverage Map** (tracks which topics have been covered)

---

#### Algorithm Workflow

After each question-answer interaction, the system performs the following steps:

1. **Update Performance Score**  
   The system updates the performance score using a weighted moving average, giving higher importance to recent responses.

2. **Check for Level Advancement**  
   If the performance score exceeds a predefined threshold (e.g., 70%) and the student has answered at least three questions at the current level, the system moves to the next Bloom's level.

3. **Check for Level Reduction**  
   If the performance score falls below a lower threshold (e.g., 40%), the system reduces the level and revisits the concept with simpler questions.

4. **Concept Coverage Check**  
   The system ensures that questions are not repeated unnecessarily.  
   However, if a misconception is detected, the system revisits that concept using a different questioning approach.

---

#### Key Feature

This adaptive mechanism ensures that:
- Strong students are continuously challenged  
- Struggling students receive simpler, supportive questions  
- Learning remains personalized and efficient  
