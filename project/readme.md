# Little Professor Game in Python
#### Video Demo: [Insert URL Here]
#### Description:

This is a python program which simulates the Little Professor game. The Little Professor Game is a game designed to enhance the mental math skills of children aged 5 to 9. It presents
math expressions challenging the players to solve them, thereby providing an enjoyable gaming experience while fostering learning and development

### Project Structure:

#### `project.py`

The core functionality of the Little Professor Game resides in project.py. This script contains a collection of essential helper functions responsible for input validation, level-based random number generation, mathematical operation execution, and random operation generation

The script begins with an introduction and guidelines for the game, providing players with essential information about the game's purpose and how it operates, such as how it handles division by zero problems. It clearly outlines that the Little Professor Game generates unsolved math expressions and challenges players to find the correct answers. The goal is to encourage players to solve as many math problems and score as highly as possible. The introduction also includes rules, such as the choice of difficulty levels and the consequences of incorrect answers.

The core of the script revolves around the main game loop, which is wrapped within the `main()` function. This loop facilitates the entire game flow. It runs each aspect of the game, from problem generation and scoring to user input handling and feedback. After completing ten math problems, the script provides an overall score and encourages players to continue playing or exit.

The `run_professor()` function holds the game's logic. Within this function, the script generates random math problems, checks the player's answers, manages scoring, and affords players the opportunity to retry problems they answered incorrectly. The design includes support for varying difficulty levels, ensuring that players can select the number of digits in the generated numbers according to their skill level.

The script incorporates robust user input handling through the `input_check()` function. It ensures that input is valid, accepting only numeric values. The script anticipates potential errors, gracefully handling exceptions and prompting users to try again when they enter invalid input.

To generate diverse and challenging math problems, the script utilizes random number generation in the `generate_integer()` function. This function produces random integers, with the level of difficulty determining whether they are single-digit, double-digit, or triple-digit numbers. The code makes use of the random library in the `generate_operation()` function, which can return one of the four basic arithmetic operations randomly.

The `operation()` function is responsible for executing the chosen arithmetic operation on two numbers and returning the result. By encountering tricky situations such as the divide by zero problem or the recurring decimal problem, It ensures that the game continues smoothly by either returning 0 or rounding the result to three decimal places.


#### `test_project.py`

The first test function, `test_input_check()`, focuses on the strength the input validation process. It utilizes Python's `unittest.mock` library to simulate user input during testing. The test suite covers multiple scenarios, including valid input and progressively more complex cases involving invalid inputs. This comprehensive testing ensures that the `input_check() `function robustly handles various forms of user input, maintaining game robustness during actual gameplay.

Next, the `test_get_level()` function evaluates the `get_level()` function. Employing a similar approach with mock input, it simulates user choices regarding the game's difficulty levels. These tests encompass a range of scenarios, from valid input to progressively more complex situations involving invalid or erroneous choices. The goal is to verify that the `get_level()` function accurately interprets user preferences and delivers the appropriate difficulty level, ensuring tailored math challenges for players.

The third test function, `test_generate_integer()`, examines the `generate_integer()` function's ability to produce random numbers within specified difficulty levels. It verifies that the generated numbers align with intended ranges for single-digit, double-digit, and triple-digit numbers. This comprehensive testing ensures the game consistently presents math problems of varying complexity to players.

The fourth function, which is the `test_operation()` function, its purpose is to verify the correctness of the `operation()` function. This battery of tests covers a spectrum of arithmetic operations, including addition, subtraction, multiplication, and division. The tests explore both straightforward scenarios and edge cases, such as division by zero. Through these tests, the script ensures that the `operation()` function accurately executes mathematical operations and gracefully handles potential challenges during gameplay.

Finally, the `test_generate_operation()` function evaluates the random operation generation capability of the `generate_operation()` function. It confirms that the function reliably selects one of the four basic arithmetic operations (addition, subtraction, multiplication, or division) in a randomized manner. This test suite safeguards the game's unpredictability and diversity, ensuring players consistently encounter engaging math challenges.


To run the tests, please run `pytest test_project.py` in your terminal

#### `requirements.txt`

This file mentioj

Enjoy playing and learning with the Little Professor Game in Python!