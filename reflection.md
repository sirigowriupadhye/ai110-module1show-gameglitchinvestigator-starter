# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").

I noticed that the game had some problems when I first ran it. The higher and lower hints were sometimes backwards. The New Game button also did not properly reset the game after it ended. I also noticed that the hint did not always appear when I expected it to.

**Bug Reproduction Log**

Document at least 3 bugs you found. Add rows as needed.

| Input | Expected Behavior | Actual Behavior | Console Output / Error |
|-------|-------------------|-----------------|------------------------|
|Guess of 2 with secret 96 |user should guess higher |Game displayed "GO LOWER!" |None |
|Guess of 19 when secret was 19 | ame should recognize the correct guess and show a success| Game displayed “Game over. Start a new game to try again.”| None|
|Wrong guess with "Show hint" checked | A high/low hint should appear| No hint appeared| None|

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
- Give one example of an AI suggestion you did not accept as written (including what the AI suggested, why you rejected or changed it, and how you verified your version). It does not have to be a suggestion that was wrong: over-engineered, out of scope, harder to read, or a poor fit for this codebase all count.

I used ChatGPT to help me understand the code and find bugs in the game. One suggestion that was correct was fixing the secret number so the higher/lower hint would work correctly. I tested the game myself to make sure the fix worked. One suggestion I did not use exactly was adding more complicated changes to the game. I kept my code simple and easier to understand. I tested my changes with different guesses to make sure the game worked correctly.

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
- Did AI help you design or understand any tests? How?

I decided a bug was fixed by testing the same situation again and checking if the game worked correctly. I tested the higher/lower hint with a secret of 67 and a guess of 60, and it correctly said “Go HIGHER!”.I also tested the New Game button after the game ended, and it correctly reset the game. AI helped me understand what to test and why the changes fixed the bugs.

---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?

I learned that Streamlit reruns the Python code from the beginning whenever the user interacts with the app, such as clicking a button. Session state allows information such as the secret number, attempts, score, and game status to stay available between those reruns. Without session state, the game would lose important information whenever the page reruns. This helped me understand why resetting the session state correctly was important when fixing the New Game bug.

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
- In one or two sentences, describe how this project changed the way you think about AI generated code.

One habit I want to use in future projects is testing my code after I make changes. I also want to understand what AI suggests before using it. Next time, I will ask AI more specific questions so the answers are easier to follow. This project taught me that AI can make mistakes, so I should always check my code myself.
