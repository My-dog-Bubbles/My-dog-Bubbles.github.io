## Number Guessing Game
```mermaid 
flowchart TD
A(Pulling up guessing game) --> B[Get random number]
B --> Z[/Welcome to the</br/>Imposiable Guesser !!!</br/>You will only get 2 chances to guess/]
Z --> Y[/If you don't guess in time then you will be kicked out =D/]
Y --> C[/Guess My number:/]
C --> D{User Guess =</br/>Computer NUM}
D --> |True| F[/Correct!!!!</br/>Do you want to play again?/]
F --> |Yes| Z
F --> |No| O(Ok, bye bye)
D --> |False| X{User Guess ></br/>Computer NUM}
X --> |TRUE| E[/That is wrong, Too high. </br/>You have 1 more guesses/]

E --> G{User Guess =</br/>Computer NUM}
G --> |False| H(Wrong =<</br/>Bye Bye)
G --> |True| I[/Correct do you want to play again/]
I --> |Yes| Z
I --> |No| N(Ok, bye bye)
X --> |FALSE| R[/That is wrong, Too Low. </br/>You have 1 more guesses/]
R --> J{User Guess =</br/>Computer NUM}
J --> |False| L(Wrong =<</br/>Bye Bye)
J --> |True| K[/Correct!!!!</br/>Do you want to play again?/]
K --> |Yes| Z
K --> |No| M(Ok, bye bye!)

```