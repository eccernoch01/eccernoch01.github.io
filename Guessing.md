```mermaid
flowchart TD
 A[Get the lower range value.] --> B[Get the upper range value.];
 B[Get the upper range value] --> C[Select a number within range.];
 C[Select a number within range.] --> D[Let the player submit a guess.];
 D[Let the player submit a guess.] --> E@{ shape: diamond, label: "Is the guess the same as the number?" };
 E@{ shape: diamond, label: "Is the guess the same as the number?" } --> E1[Yes];
 E@{ shape: diamond, label: "Is the guess the same as the number?" } --> E2[No];
 E1[Yes] --> Final[YOU WIN];
 Final[YOU WIN] --> A;
 E2[No] --> F@{ shape: diamond, label: "Is the guess a number, and within range?"};
 F@{ shape: diamond, label: "Is the guess a number, and within range?"} --> F1[Yes];
 F@{ shape: diamond, label: "Is the guess a number, and within range?"} --> F2[No];
 F2[No] --> D;
 F1[Yes] --> G[Is the guess > the number?];
 G[Is the guess > the number?] --> G1[Yes];
 G[Is the guess > the number?] --> G2[No];
 G1[Yes] --> H1[Guess is too high!] --> D;
 G2[No] --> H2[Guess is too low!] --> D;
```
# Flowchart Description
## Above is a basic flowchart that follows the steps to play the number game. First the lower and upper range are set by the user, followed by a guess from the player. From there, the computer determines if the guessed number is the same as the randomly selected one, if it is, then the player is sent back to the start to set a new range for the next game. If the number is incorrect, the program then checks to see if the guess is even a number, and if it is under the max, and over the min. If the guess is invalid, the player is sent back to guess again. If the guess is a number within the range, the program then checks if the guess is > the random selection. If it is greater or lower, the player is notified and then sent back to guess again.
