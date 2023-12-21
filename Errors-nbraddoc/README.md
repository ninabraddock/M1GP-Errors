# Errors
This project is riddled with errors. Please fix all the bugs!

## Setup
Use this Guided Project template to create a new repository (see [GitHub-with-CLion](https://github.com/uvmcs2300f2023/GitHub-with-CLion) repo for directions).
**Your repository must be named with the convention: Errors-netid**, where netid is your UVM NetID username.

When you first put it into CLion, the Build and Run buttons will be grayed out and unclickable. This is intentional. You will need to start fixing bugs before these buttons can be used.

Remember to commit and push frequently.

## Errors
There are three types of errors:
1. **Compiler errors** prevent your program from running. These are typically CMake or syntax errors.
1. **Runtime errors** occur while the program is running and prevent an exit code of zero. Examples of this include a non-zero exit code and an infinite loop.
1. **Logic errors** are when your program runs to completion (with exit code zero) but does not behave the way you intended. The best way to catch logic errors is through extensive testing and/or the use of the debugger.

For this project, you have been given a very broken program and it is your job to fix it. For each error you fix, log it in the table below.

## Logging Errors
Every time you fix a bug, log it in the README file here:

| Type of error (compiler, runtime, logic) | File           | Description                                                                                                                                                     | Fix                                                                  |
|------------------------------------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| Example: compiler                        | CMakeLists.txt | "project PROJECT called with incorrect number of arguments"                                                                                                     | Added the project name to line 2                                     |
| Compiler Line 26                         | main.cpp       | if else statement                                                                                                                                               | changed second if to else if                                         |
| Compiler Line 9                          | spie.cpp       | deleted duplicate add_winning_number(); function call                                                                                                           |                                                                      |
| Compiler Line 15                         | spie.cpp       | add () around MAX_NUMBERS +1 for initializing new_number                                                                                                        |                                                                      |
| Compiler Line 31                         | spie.cpp       | changed the double or operators to single in the while loop                                                                                                     |                                                                      |
| Compiler Line 32                         | spie.cpp       | deleted the first endl in the middle of the print statement to console                                                                                          |                                                                      |
| Compiler Line 61                         | spie.cpp       | added endl to the winning numbers print statement                                                                                                               |                                                                      |
| Compiler Line 7                          | main.cpp       | add method () on the end of game.print_winning_numbers                                                                                                          |                                                                      |
| Compiler Line 12                         | main.cpp       | add open curly brace to switch expression                                                                                                                       |                                                                      |
| Compiler Line 51                         | main.cpp       | missing ";" at the end of return 0                                                                                                                              |                                                                      |
| Compiler                                 | spie.h         | " 'ostream' has not been declared " error message                                                                                                               | added #include <fstream> to be able to use ostream                   |
| Compiler                                 | spie.h         | incorrect vector instantiation used                                                                                                                             | changed vector winning_numbers to std::vector <int> winning_numbers; |
| Compiler                                 | main.cpp       | "expected unqualified-id before ')' token"                                                                                                                      | added game onto function, SPIE_Game game();                          |
| Compiler                                 | main.cpp       | "error: request for member 'print_winning_numbers' in 'game', which is of non-class type 'SPIE_Game()'game.print_winning_numbers();                             | added parameters "ostream &outs"                                     |
| Compiler                                 | spie.h         | "error: candidate is: static char SPIE_Game::get_player_choice(int&, int&)static char get_player_choice(ostream &outs, istream &ins);"                          | added std:: in front of ostream and istream                          |
| Compiler                                 | spie.h         | "error: 'ostream' has not been declared void print_winning_numbers(ostream &outs) const;                                                                        | add std:: to ostream &outs parameter                                 |
| Compiler                                 | main.cpp       | "error: request for member 'print_winning_numbers' in 'game', which is of non-class type 'SPIE_Game()'game.print_winning_numbers(ostream &outs);                | added std:: to "ostream & outs"                                      |
| Compiler                                 | spie.h         | "error: request for member 'print_rules' in 'game', which is of non-class type 'SPIE_Game()'game.print_rules(cout);                                             | added SPIE_Game:: to the front of SPIE_Game() {                      |
| Compiler                                 | main.cpp       | multiple errors " error: request for member 'get_player_choice' in 'game', which is of non-class type 'SPIE_Game()'choice = game.get_player_choice(cout, cin);" | just added the :: onto the end of SPIE_Game                          |
| Compiler                                 | main.cpp       | "error: expected primary-expression before '&' token game.print_winning_numbers(std::ostream &outs);                                                            | deleted std::ostream from game.print_winning_numbers(outs);          |
| Compiler                                 | main.cpp       | changed inside of print_winning_numbers() method call                                                                                                           | game.print_winning_numbers(std::cout);                                                                     |







### Grading Rubric
- [ ] (2 pts) Fix at least one CMake compiler error (not including the one already given).
- [ ] (3 pts) Fix at least one other compiler error.
- [ ] (3 pts) Fix at least one runtime error.
- [ ] (3 pts) Fix at least one logic error.
- [ ] (5 pts) The README table is populated fully and correctly.
- [ ] (4 pts) Fix at least 15 errors total (note: errors you create do not count lol).
