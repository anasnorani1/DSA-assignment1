------------------------------------------------------------
              DSA Assignment 1 - Fall 2025
------------------------------------------------------------

Name: Anas Norani  
Reg. No: 501231  
Course: Data Structures & Algorithms  
Institute: NUST  
Semester: Fall 2025  

------------------------------------------------------------
📚 OVERVIEW
------------------------------------------------------------

This assignment demonstrates the application of **core data structures**
to real-world inspired problems using **Object-Oriented Programming (OOP)**
in C++. The solutions strictly adhere to the provided header files
without modification and emphasize correctness, modularity, and efficiency.

The assignment includes three major tasks:
1. Polynomial Abstract Data Type (ADT)
2. Text Editor Simulation
3. UNO Game Simulation

Each problem uses a **different data structure** suited to its context,
highlighting a strong understanding of design and algorithmic thinking.

------------------------------------------------------------
🧩 PROBLEM 1: Polynomial ADT
------------------------------------------------------------

🔹 **Approach:**
A polynomial is represented as a **linked list** where each node stores a term’s
coefficient and exponent. Terms are maintained in **descending order** of exponent.
Duplicate powers are merged automatically, and zero terms are removed dynamically.

🔹 **Data Structure Used:**  
→ **Linked List** (manually implemented using a node structure)

🔹 **Core Operations:**
- `insertTerm(int c, int e)`: Inserts or merges terms while maintaining order.
- `add(const Polynomial& other)`: Combines two polynomials by traversing linked lists.
- `multiply(const Polynomial& other)`: Multiplies all term pairs and merges like powers.
- `derivative()`: Computes the derivative using exponent rules.
- `toString()`: Converts polynomial into readable string (e.g. “3x^2 + 2x - 5”).

🔹 **Corner Cases Handled:**
- Insertion of duplicate exponents → terms merged correctly.
- Coefficient becomes zero → term automatically removed.
- Empty polynomial → outputs “0”.

🔹 **Challenges:**
Maintaining sorted insertion order while merging terms and ensuring memory
is correctly managed without leaks.

------------------------------------------------------------
⌨️ PROBLEM 2: Text Editor Simulation
------------------------------------------------------------

🔹 **Approach:**
A **cursor-based text editor** is simulated using **two stacks** (or equivalent logic).
The left stack represents characters before the cursor, and the right stack
represents characters after it. This allows **O(1)** insertion, deletion,
and cursor movement operations.

🔹 **Data Structure Used:**  
→ **Two Stacks**

🔹 **Core Operations:**
- `insertChar(char c)`: Inserts character at cursor.
- `deleteChar()`: Deletes character before cursor (backspace behavior).
- `moveLeft()` / `moveRight()`: Moves cursor left/right safely.
- `getTextWithCursor()`: Returns text with cursor represented by `|`.

🔹 **Corner Cases Handled:**
- Deleting when cursor at start → safely ignored.
- Cursor movements beyond boundaries → prevented.
- Empty editor → displays as “|”.

🔹 **Challenges:**
Maintaining synchronization between left and right stacks for cursor position
and ensuring correct display after every operation.


------------------------------------------------------------
🎮 PROBLEM 3: UNO Game Simulation
------------------------------------------------------------

🔹 **Approach:**
Implemented a simplified **UNO Game** supporting special cards (Skip, Reverse, Draw Two)
and automatic play turn logic. The game uses **vectors** for the deck, discard pile,
and player hands. Each turn follows UNO rules, updating direction and skipping
appropriately.

🔹 **Data Structure Used:**  
→ **Vectors** for dynamic storage of cards, players, and piles.

🔹 **Core Operations:**
- `UNOGame(int numPlayers)`: Initializes game with given players.
- `initialize()`: Creates, shuffles (fixed seed = 1234), and deals cards.
- `playTurn()`: Plays a full valid turn (Skip, Reverse, Draw Two handled).
- `isGameOver()`: Returns true when a player has no cards left.
- `getState()`: Displays formatted game state and top card.

🔹 **Corner Cases Handled:**
- Handling “Draw Two” when deck has fewer than two cards.
- Consecutive Reverse/Skip combinations.
- Detecting and declaring winner correctly.
- Preventing invalid moves (must match color or value).


------------------------------------------------------------
🎮 PROBLEM 3: UNO Game Simulation
------------------------------------------------------------

🔹 **Approach:**
Implemented a simplified **UNO Game** supporting special cards (Skip, Reverse, Draw Two)
and automatic play turn logic. The game uses **vectors** for the deck, discard pile,
and player hands. Each turn follows UNO rules, updating direction and skipping
appropriately.

🔹 **Data Structure Used:**  
→ **Vectors** for dynamic storage of cards, players, and piles.

🔹 **Core Operations:**
- `UNOGame(int numPlayers)`: Initializes game with given players.
- `initialize()`: Creates, shuffles (fixed seed = 1234), and deals cards.
- `playTurn()`: Plays a full valid turn (Skip, Reverse, Draw Two handled).
- `isGameOver()`: Returns true when a player has no cards left.
- `getState()`: Displays formatted game state and top card.

🔹 **Corner Cases Handled:**
- Handling “Draw Two” when deck has fewer than two cards.
- Consecutive Reverse/Skip combinations.
- Detecting and declaring winner correctly.
- Preventing invalid moves (must match color or value).


------------------------------------------------------------
🧠 DATA STRUCTURES SUMMARY
------------------------------------------------------------

🔹 **Challenges:**
- Strictly adhering to uneditable header files while designing efficient internal logic.

- Balancing readability, correctness, and modularity in C++ code.

- Managing dynamic memory safely (especially in the polynomial problem).

- Ensuring that outputs exactly matched the provided sample outputs.

- Using version control (GitHub) effectively to track and organize changes.

- Designing a realistic flow with direction toggling, skip behavior,
and ensuring top card formatting (e.g. “Red Skip”, “Blue 3”) matches the expected output.

| Problem        | Data Structure | Purpose                                  |
|----------------|----------------|------------------------------------------|
| Polynomial     | Linked List     | Efficient term insertion and combination |
| Text Editor    | Two Stacks      | O(1) cursor operations                   |
| UNO Game       | Vector          | Dynamic card and player management       |

------------------------------------------------------------
💻 COMPILATION & EXECUTION
------------------------------------------------------------

Compile and run each task separately:

```bash
g++ polynomial.cpp main1.cpp -o polynomial
./polynomial

g++ texteditor.cpp main2.cpp -o texteditor
./texteditor

g++ uno.cpp main3.cpp -o uno
./uno

