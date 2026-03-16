# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?

When I first ran the game, the interface appeared and I could enter guesses, but some features were not working properly. The “New Game” button was visible, but clicking it did not reset or start a new round, so the game could not restart from the interface.

- List at least two concrete bugs you noticed at the start  
  (for example: "the secret number kept changing" or "the hints were backwards").

i. Incorrect hint direction. For example, if the secret number was 25 and I guessed 26, the game told me to guess higher, which is incorrect. Since 26 is greater than 25, the program should have told me to guess lower. The same issue happened in reverse when guessing a smaller number.

ii. Incorrect attempt counter. The game displayed that I was out of attempts even though I still had one attempt remaining, which meant the counter logic was off and did not correctly track the number of guesses left.

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
Claude

- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).

I refractored the code using AI and verfied by line by line inspection with the previous code.

- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).

The AI suggested some code for conftest.py and it seemed complicated and I didn't understand it so I rejected the code and searched the web and other AI tools myself to verify that it was working, I checked if the tests are up and running.

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
I ran the test cases and it passed.

- Describe at least one test you ran (manual or using pytest) and what it showed you about your code.

I ran a pytest to test_winning_guess and it taughted me to be specific about what to test on based on the exisitng code logic.

- Did AI help you design or understand any tests? How?
AI helped me understand the tests with the code it gave. I realised the code was missing the one crucial part which seem minor but the useful one.

---

## 4. What did you learn about Streamlit and state?

- In your own words, explain why the secret number kept changing in the original app.
It's because the reset logic wasn't working and also, it didn't clear out the history.

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
The session state in streamlit is a varaible that stores variables values and when it reruns, those variables are not changed unless changed deliberrately. This preserves the state.

- What change did you make that finally gave the game a stable secret number?
I changed the 'new game' button logic and it gave me a stab;e secret number.


---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
In future labs or projects, I wanna use the prompting strategy and most importantly testimg habit. I also try to see passing and failing cases while writing the methods and write the tests accordingly. 

- What is one thing you would do differently next time you work with AI on a coding task?
I feel like i sometimes do not explain AI nicely about the problem. I would like to be more specific with AI on what to fix. Also learning about the changes and having informed changed despite the AI help will help me in the future.

- In one or two sentences, describe how this project changed the way you think about AI generated code.
AI generated code can be very helpful if one can prompt what they need exact and how they want it to be. For this to happen, one must be able to follow through the AI code during development deliberately, otherwise we might miss the context and would eventually be in a rabbithole of failure and debugging.