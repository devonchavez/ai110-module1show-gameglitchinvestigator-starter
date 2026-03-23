# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
- List at least two concrete bugs you noticed at the start.
  (for example: "the secret number kept changing" or "the hints were backwards").

  1 bug I noticed was that the game was inccorectly advising me how much bigger or smaller to target each guess the more I tried, for instance if the secret number was 30 and I guessed 2 the game was telling me to guess lower. Another bug I noticed was that the different difficulty options werent working. Id press easy and be expected to guess a number between 1-20 but the secret numbers would still be completely randomized between 1-100.

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).

I used copilot as an agent to help me make the fixes I needed in my code. 1 example of an AI suggestion that was accurate to the desired outputs I wanted were the hints being flipped. One of the bugs was that whenever a hint was given after a guess it wouldnt be accurate to what was needed to point the user towards the right direction. For example if the target number was 80 and the user guessed 20 the suggestion that followed was to guess lower which would have been an incorrect statement. An example of when AI made an edit that was misleading was in the beginning when I had it refactor the logic. I initially wanted it to only move the logic to its right places but it had also started making edits at the same time, which was a good choice but I didnt want too much to be happening and a better transition from seeing what exactly had moved and not a combination of having to check what had been moved AND fixed. I was able to ask copilot to ONLY move the code and not start on any of the fixes yet. 

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
- Did AI help you design or understand any tests? How?

I was able to decide whether the bug was acutally fixed by reloading the website after saving the changes. I was able to manualling check if the difficulty was accurately depicting the range that corresponded with the difficulty by constantly creating a new game and seeing the new target number that was in the debuggers info. AI helped me understood the tests but I felt the fixes were also easily noticeable from my eyes.

---

## 4. What did you learn about Streamlit and state?

- In your own words, explain why the secret number kept changing in the original app.
- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
- What change did you make that finally gave the game a stable secret number?

I think the secret number kept changing because it created a new gameloop letting the user play over and over if they wanted. I fixed the hard coded value of the target guess to the low and high so that it corresponded correctly to the difficulty selected.

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
- In one or two sentences, describe how this project changed the way you think about AI generated code.

I want to reuse the test case feature. Having AI run test cases saves a lot of time than having to do them by hand. I wish I would be more specific and intentional with what I wanted AI to do, it was really easy to get carried away and kind of "get a feel" that the code was right form just skimming and not thouroughly checking. This project helped me be more intentional with how to search for bugs and using AI generated code to give me a foundation on what needs to be fixed but not exacty always accurate so it always needs to be checked/ verified.