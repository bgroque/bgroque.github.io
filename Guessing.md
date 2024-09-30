```mermaid
flowchart TD
 A[Start Game] --> B[Generate Random Number 1-100]
 B --> C[Get User Input]
 C --> D{Is Input A Number?}
 D -- No --> E[Invalid Input]
 D -- Yes --> F{Is Guess Within Range?}
 F -- No --> E
 E --> D
 F -- Yes --> G{Correctly Guessed?}
 G -- Yes --> H[Congratulations You Win! End Game]
 G -- No --> I{Feedback}
 I -- Too High --> J[Try Lower]
 I -- Too Low --> K[Try Higher]
 J & K --> C

The flowchart starts by getting a number and asking the user to guess the number
If the user input is not a number, their input is invalid and they will be looped back to try again
If the input is a number, the program will check to see if they're correct
If the user input is too high, they will get a "Try Lower" suggestion and will be looped back to "Get User Input"
If the user input is too low, they will get a "Try Higher" suggestion and will be looped back to "Get User Input"
Finally, if the user guesses correctly, they get a congratulations message and the game ends.
I used braces{} a lot to make it clear when there are multiple outcomes.
