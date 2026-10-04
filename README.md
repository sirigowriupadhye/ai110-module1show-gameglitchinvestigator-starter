# 🎮 Game Glitch Investigator: The Impossible Guesser

## 🚨 The Situation

You asked an AI to build a simple "Number Guessing Game" using Streamlit.
It wrote the code, ran away, and now the game is unplayable. 

- You can't win.
- The hints lie to you.
- The secret number seems to have commitment issues.

## 🛠️ Setup

1. Install dependencies: `pip install -r requirements.txt`
2. Run the broken app: `python -m streamlit run app.py`

## 🕵️‍♂️ Your Mission

1. **Play the game.** Open the "Developer Debug Info" tab in the app to see the secret number. Try to win.
2. **Find the State Bug.** Why does the secret number change every time you click "Submit"? Ask ChatGPT: *"How do I keep a variable from resetting in Streamlit when I click a button?"*
3. **Fix the Logic.** The hints ("Higher/Lower") are wrong. Fix them.
4. **Refactor & Test.** - Move the logic into `logic_utils.py`.
   - Run `pytest` in your terminal.
   - Keep fixing until all tests pass!

## 📝 Document Your Experience

- [ ] Describe the game's purpose.
The game is a number guessing game where the player tries to guess a secret number. The game gives hints to tell the player whether their guess is too high or too low.
- [ ] Detail which bugs you found.
I found two main bugs. The higher and lower hints were backwards, the game did not properly reset when starting a new game.
- [ ] Explain what fixes you applied.
I fixed the game logic so the higher and lower hints correctly match the player's guess. I also fixed the game state so the secret number stays the same while playing and resets when starting a new game. The guessing logic was moved into `logic_utils.py`, and I added automated tests for winning, too high, and too low guesses.

## 📸 Demo Walkthrough

Describe your fixed game in numbered steps so a reader can follow along without watching a video:

1. The player starts a new game and the game chooses a secret number.
2. The player enters a guess that is lower than the secret number.
3. The game correctly shows "Go HIGHER!".
4. The player enters a guess that is higher than the secret number, and the game correctly shows "Go LOWER!".
5. The player enters the correct secret number and the game shows the winning result.
6. The player can start a new game, which resets the game state and chooses a new secret number.

**Screenshot** *(optional)*: <!-- Insert a screenshot of your fixed, winning game here -->

## 🧪 Test Results

```
# Paste your pytest output here, e.g.:
# pytest tests/
# collected 3 items                                                              

tests\test_game_logic.py ...                                             [100%]

============================== 3 passed in 0.10s ==============================
```

## 🚀 Stretch Features

- [ ] [If you choose to complete Challenge 4, describe the Enhanced UI changes here — a screenshot is optional]
