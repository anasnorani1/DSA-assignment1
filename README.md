------------------------------------------------------------
              DSA Assignment 1 - Fall 2025
------------------------------------------------------------

Name: Anas Norani  
Course: Data Structures and Algorithms  
Institute: NUST  
Semester: Fall 2025  

------------------------------------------------------------
📘 Approach
------------------------------------------------------------

This assignment consists of three independent problems designed to demonstrate
understanding and application of data structures through Object-Oriented Programming in C++.

1. **Problem 1 – Polynomial ADT**
   - **Approach:** Implemented a polynomial using a **linked list** where each node stores
     a coefficient and exponent. The list remains sorted in descending order by exponent.
     Duplicate exponents are merged automatically.
   - **Key Operations:** insertTerm, add, multiply, derivative, toString.
   - **Data Structure:** Linked List.
   - **Reasoning:** Linked lists allow efficient insertion and deletion of polynomial terms,
     especially when combining or differentiating.

2. **Problem 2 – Text Editor Simulation**
   - **Approach:** Simulated a basic text editor with cursor functionality using **two stacks**:
     the left stack holds text before the cursor, and the right stack holds text after it.
     This enables O(1) cursor movement and character insertion/deletion.
   - **Key Operations:** insertChar, deleteChar, moveLeft, moveRight, getTextWithCursor.
   - **Data Structure:** Two Stacks.
   - **Reasoning:** Using two stacks mirrors how real text editors manage text around the cursor
     efficiently, avoiding costly string shifts.

3. **Problem 3 – UNO Game Simulation**
   - **Approach:** Designed a simplified UNO game using **vectors** to represent decks,
     player hands, and the discard pile. Game logic supports Skip, Reverse, and Draw Two cards,
     with direction and turn order managed dynamically.
   - **Key Operations:** initialize, playTurn, isGameOver, getState.
   - **Data Structure:** Vectors.
   - **Reasoning:** Vectors provide dynamic resizing and easy iteration, ideal for managing
     changing card sets and game flow.
   - **Sample Output Example:**
     ```
     Player 0's turn, Direction: Clockwise, Top: Blue 3, Players cards: P0:7, P1:7
     Player 1's turn, Direction: Clockwise, Top: Blue 8, Players cards: P0:7, P1:6
     Player 0's turn, Direction: Clockwise, Top: Yellow 8, Players cards: P0:6, P1:6
     Player 0's turn, Direction: Clockwise, Top: Yellow Skip, Players cards: P0:5, P1:6
     ```

------------------------------------------------------------
🌐 Publicly Accessible GitHub Link
------------------------------------------------------------

GitHub Repository:  
👉https://github.com/anasnorani1/DSA-assignment1

The repository includes all source files (`.cpp`, `.h`, and driver files)
with clear commit history and meaningful commit messages demonstrating progressive development.

------------------------------------------------------------
💡 Challenges Faced
------------------------------------------------------------

**Problem 1 – Polynomial ADT**
- Managing sorted insertion while merging like terms.
- Handling memory safely to avoid leaks when removing or combining nodes.
- Formatting string output correctly for negative coefficients and zero terms.

**Problem 2 – Text Editor**
- Keeping cursor movement synchronized between two stacks.
- Preventing out-of-bound cursor movements.
- Ensuring correct display after complex edit sequences.

**Problem 3 – UNO Game**
- Implementing direction change (Reverse) and Skip logic correctly.
- Handling Draw Two and ensuring the next player receives extra cards.
- Managing the game state format so output matches exactly the required style (e.g., “Top: Red Skip”).
- Ensuring deterministic results using a fixed shuffle seed.

**General Challenges**
- Writing efficient logic under the constraint of unmodifiable header files.
- Balancing correctness, modularity, and readability in C++.
- Testing multiple edge cases to ensure robustness across all tasks.

------------------------------------------------------------
✅ End of README
------------------------------------------------------------
