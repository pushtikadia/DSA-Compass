# 🗺️ Data Structures & Algorithms Roadmap

This roadmap is designed to take you from the basics of programming to advanced interview preparation, covering essential data structures, algorithms, and problem-solving techniques.

---

## 🏁 Phase 1: The Prerequisites
Before diving into DSA, ensure you are comfortable with the syntax and basics of one coding language.

- [ ] **Choose a Programming Language** (Python, Java, C++, JavaScript, etc.)
- [ ] Understand Variables, Loops, and Conditions
- [ ] Understand Functions and Classes

---

## 🏗️ Phase 2: Data Structures (The Building Blocks)
Learn how data is stored and organized.



### 2.1 🧱 Linear Data Structures
Sequential organization of data.

**1. Arrays (Static & Dynamic)**
- [ ] **Basics:** Understanding contiguous memory allocation & Indexing.
- [ ] **Operations:** Insert, Delete, Update, Traversal ($O(1)$ vs $O(N)$).
- [ ] **Dynamic Arrays:** Implementing automatic resizing (like `ArrayList` in Java or `vector` in C++).
- [ ] **2D Arrays / Matrices:** Row-major vs Column-major order.
- [ ] **Techniques:** Prefix Sum Arrays, Sliding Window on Arrays.

**2. Linked Lists**
- [ ] **Singly Linked List:** Node structure (Data + Next Pointer).
- [ ] **Doubly Linked List:** Handling `Prev` and `Next` pointers.
- [ ] **Circular Linked List:** Last node pointing back to Head.
- [ ] **Core Operations:**
    - [ ] Insertion (Head, Tail, Middle).
    - [ ] Deletion (Head, Tail, Middle).
    - [ ] Reversing a Linked List (Iterative & Recursive).
- [ ] **"Runner" Technique:** Fast & Slow pointers (Tortoise & Hare) for finding middle or detecting cycles.

**3. Stacks (LIFO - Last In, First Out)**
- [ ] **Implementation:** Using Arrays vs. Using Linked Lists.
- [ ] **Core Operations:** Push, Pop, Peek/Top, IsEmpty.
- [ ] **Monotonic Stack:** Finding "Next Greater Element" or "Previous Smaller Element".
- [ ] **Applications:**
    - [ ] Valid Parentheses checking `()[]{}`.
    - [ ] Expression Conversion (Infix to Postfix/Prefix).
    - [ ] Recursion Stack visualization.

**4. Queues (FIFO - First In, First Out)**
- [ ] **Implementation:** Using Arrays vs. Linked Lists.
- [ ] **Core Operations:** Enqueue (Add), Dequeue (Remove), Front, Rear.
- [ ] **Circular Queue:** Implementing a Ring Buffer (using modulo operator `%`).
- [ ] **Double-Ended Queue (Deque):** Insertion/Deletion at both ends.
- [ ] **Priority Queue:** (Introduction only) Elements processed by priority, not arrival.



### 2.2 🌳 Non-Linear Data Structures
Hierarchical or interconnected organization of data.

**1. Trees (Hierarchical Data)**
- [ ] **Binary Trees (General):**
    - [ ] **Structure:** Root, Left Child, Right Child, Leaf Nodes.
    - [ ] **Types:** Full, Complete, Perfect, Balanced Binary Trees.
    - [ ] **Traversals:**
        - [ ] Depth-First: Pre-order, In-order, Post-order (Iterative & Recursive).
        - [ ] Breadth-First: Level-order traversal (using Queue).
    - [ ] **Standard Problems:** Height of tree, Diameter of tree, Lowest Common Ancestor (LCA).

- [ ] **Binary Search Trees (BST):**
    - [ ] **Property:** Left < Root < Right.
    - [ ] **Operations:** Search, Insert, Delete ($O(\log N)$ average).
    - [ ] **Validation:** Checking if a Binary Tree is a valid BST.
    - [ ] **Balancing (Concept):** Understanding why unbalanced trees degrade to Linked Lists ($O(N)$).

- [ ] **Heaps (Priority Queues):**
    - [ ] **Types:** Min-Heap (smallest at top) vs. Max-Heap (largest at top).
    - [ ] **Implementation:** Binary Heap using Arrays (Index math: `2i+1`, `2i+2`).
    - [ ] **Operations:** Push, Pop (Extract Min/Max), Heapify, Decrease Key.
    - [ ] **Usage:** Finding "K-th" largest/smallest elements efficiently.

**2. Graphs (Network Data)**
- [ ] **Representation (How to store them):**
    - [ ] **Adjacency Matrix:** 2D Array (Good for dense graphs).
    - [ ] **Adjacency List:** Array of Lists/Vectors (Standard for interviews).

- [ ] **Graph Types:**
    - [ ] **Directed:** One-way streets (e.g., Web page links).
    - [ ] **Undirected:** Two-way streets (e.g., Facebook friends).
    - [ ] **Weighted:** Edges have cost/distance (e.g., Google Maps).
    - [ ] **Cyclic vs. Acyclic:** Detection of loops.

- [ ] **Core Algorithms:**
    - [ ] **Traversal:** BFS (Shortest path in unweighted) vs. DFS (Path finding/Backtracking).
    - [ ] **Cycle Detection:** Using DFS (Recursion stack) or Disjoint Set (Union-Find).
    - [ ] **Topological Sort:** Ordering tasks with dependencies (Directed Acyclic Graphs only).

- [ ] **Advanced Graph Algorithms (The "Hard" Questions):**
    - [ ] **Dijkstra’s Algorithm:** Shortest path in weighted graphs (No negative weights).
    - [ ] **Bellman-Ford:** Shortest path with negative weights.
    - [ ] **Prim’s / Kruskal’s:** Minimum Spanning Tree (MST).



### 2.3 CRUD Operations
Master the basic operations for all the structures above.
- [ ] **C**reate (Insert data)
- [ ] **R**ead (Retrieve data)
- [ ] **U**pdate (Modify data)
- [ ] **D**elete (Remove data)

---





## 🔍 Phase 3: Traversal & Searching
How to navigate through your data structures.



### 3.1 🔍 Searching Algorithms

**1. Linear Search**
- [ ] **Method:** Iterate through the collection element by element.
- [ ] **Use Case:** Unsorted data or very small datasets.
- [ ] **Complexity:** Time: $O(N)$ | Space: $O(1)$.
- [ ] **Optimization:** Sentinel Linear Search (removes one check inside the loop).

**2. Binary Search (Divide & Conquer)**
- [ ] **Pre-requisite:** Data **must** be sorted.
- [ ] **Core Logic:** Compare target with `mid`; discard half the search space.
- [ ] **Implementation:**
    - [ ] **Iterative:** Using `while(low <= high)` loop (Preferred to avoid stack overflow).
    - [ ] **Recursive:** Function calls itself with new bounds.
    - [ ] **Bug-Free Mid:** Using `mid = low + (high - low) / 2` to prevent integer overflow.
- [ ] **Advanced Patterns:**
    - [ ] **Lower Bound:** Finding the *first* occurrence of a value.
    - [ ] **Upper Bound:** Finding the first value *greater* than target.
    - [ ] **Search on Answer:** Using Binary Search to find the optimal solution (e.g., "Minimum capacity to ship packages").


**3. Depth First Search (DFS)**
- [ ] **Philosophy:** "Go deep before going wide." Explore a branch as far as possible, then backtrack.
- [ ] **Data Structure:** Uses a **Stack** (or the Call Stack via Recursion).
- [ ] **Graph/Tree Applications:**
    - [ ] **Path Finding:** Finding *any* path between two nodes (e.g., Solving a Maze).
    - [ ] **Cycle Detection:** Checking if a graph contains a loop.
    - [ ] **Topological Sort:** Scheduling tasks where order matters.
    - [ ] **Connected Components:** Counting islands in a grid.

**4. Breadth First Search (BFS)**
- [ ] **Philosophy:** "Go wide before going deep." Explore all immediate neighbors before moving to the next level.
- [ ] **Data Structure:** Uses a **Queue** (FIFO).
- [ ] **Graph/Tree Applications:**
    - [ ] **Level Order Traversal:** Printing a tree row by row.
    - [ ] **Shortest Path (Unweighted):** Finding the shortest distance in a graph where all edges have equal weight (Critical Interview Question).
    - [ ] **Social Networks:** Finding "Friends of Friends" (2nd degree connections).



### 3.2 🔄 Tree Traversal Techniques

**1. Depth-First Traversals (DFS Variants)**
*These traversals go as deep as possible down one branch before backtracking.*

- [ ] **In-order Traversal (Left → Root → Right)**
    - [ ] **Process:** Visit Left Subtree, then Visit Node, then Visit Right Subtree.
    - [ ] **Key Property:** On a **Binary Search Tree (BST)**, this retrieves data in **sorted (ascending) order**.
    - [ ] **Implementation:**
        - [ ] Recursive (Standard 3-line function).
        - [ ] Iterative (Requires a **Stack**).

- [ ] **Pre-order Traversal (Root → Left → Right)**
    - [ ] **Process:** Visit Node, then Visit Left Subtree, then Visit Right Subtree.
    - [ ] **Key Use Case:** Great for **copying** a tree or generating a prefix expression (Polish notation). You see the structure "from the top down".
    - [ ] **Implementation:**
        - [ ] Recursive.
        - [ ] Iterative (Stack-based; Push Right child, then Left child).

- [ ] **Post-order Traversal (Left → Right → Root)**
    - [ ] **Process:** Visit Left Subtree, then Visit Right Subtree, then Visit Node.
    - [ ] **Key Use Case:** Great for **deleting** a tree (delete children before deleting the parent) or generating postfix expressions.
    - [ ] **Implementation:**
        - [ ] Recursive.
        - [ ] Iterative (Trickier; often uses 2 Stacks or a "visited" flag).



**2. Breadth-First Traversal (BFS Variant)**
*This traversal visits nodes level-by-level, from top to bottom, left to right.*

- [ ] **Level-order Traversal**
    - [ ] **Process:** Visit Root (Level 0), then all nodes at Level 1, then all nodes at Level 2, etc.
    - [ ] **Data Structure:** Requires a **Queue** (FIFO).
    - [ ] **Key Use Cases:**
        - [ ] Printing a tree structure visually.
        - [ ] Finding the "Right Side View" or "Left Side View" of a tree.
        - [ ] Finding the maximum width of a tree.
    - [ ] **Pattern:**
        1. Add Root to Queue.
        2. While Queue is not empty:
        3. Pop Node → Print it.
        4. Push Left Child (if exists).
        5. Push Right Child (if exists).

---





## 🔢 Phase 4: Sorting Algorithms
Techniques to rearrange data in a specific order.

**Basic & Educational**
- [ ] **Bubble Sort** (Simple, pairwise swapping)
- [ ] **Selection Sort** (Finds minimum, places at start)
- [ ] **Insertion Sort** (Builds sorted list one-by-one)
- [ ] **Cycle Sort** (Minimizes memory writes)

**Efficient ($O(N \log N)$)**
- [ ] **Merge Sort** (Divide and conquer, stable)
- [ ] **Quick Sort** (Pivot-based partitioning)
- [ ] **Heap Sort** (Uses binary heap data structure)
- [ ] **Shell Sort** (Generalized insertion sort)

**Non-Comparison / Linear ($O(N)$)**
- [ ] **Counting Sort** (Integer sorting based on keys)
- [ ] **Radix Sort** (Sorts digit by digit)
- [ ] **Bucket Sort** (Distributes elements into buckets)

**Hybrid (Real-World Defaults)**
- [ ] **TimSort** (Merge & Insertion hybrid - Python/Java default)
- [ ] **IntroSort** (Quick, Heap & Insertion hybrid - C++ default)
---





## 🧠 Phase 5: Core Algorithmic Concepts
Foundational concepts for solving complex problems.

**1. Recursion**
*The art of a function calling itself to solve smaller instances of the same problem.*
- [ ] **The Three Laws:**
    1. **Base Case:** The condition to stop recursion (prevents infinite loops).
    2. **Logic/Action:** The operation performed at the current step.
    3. **Recursive Step:** Calling the function with modified parameters (moving towards the base case).
- [ ] **Memory Model:** Understanding the **Call Stack** and "Stack Overflow" errors.
- [ ] **Tail Recursion:** Writing recursion so it can be optimized by the compiler (calling itself as the very last action).
- [ ] **Classic Problems:** Factorial, Fibonacci, Tower of Hanoi.



**2. Backtracking**
*A "brute-force" technique that builds a solution incrementally and abandons ("backtracks") a path as soon as it determines the path cannot lead to a valid solution.*
- [ ] **The Pattern:**
    1. **Choose:** Make a choice.
    2. **Explore:** Recurse with that choice.
    3. **Un-choose:** Undo the choice (backtrack) to try the next option.
- [ ] **Pruning:** Optimizing by cutting off branches of the search tree that are clearly invalid early.
- [ ] **Classic Problems:**
    - [ ] N-Queens Problem (Placing N queens on a chessboard).
    - [ ] Sudoku Solver.
    - [ ] Generating all Permutations/Subsets of a list.
    - [ ] Rat in a Maze.



**3. Dynamic Programming (DP)**
*Optimizing recursion by storing results of expensive function calls and re-using them later (Time-Space Tradeoff).*
- [ ] **Core Properties:**
    - [ ] **Overlapping Subproblems:** The problem breaks down into smaller problems that are repeated (e.g., Fibonacci calculating `fib(3)` multiple times).
    - [ ] **Optimal Substructure:** The optimal solution can be constructed from optimal solutions of its subproblems.
- [ ] **Two Approaches:**
    - [ ] **Memoization (Top-Down):** Recursive + Caching (storing results in a Hash Map/Array).
    - [ ] **Tabulation (Bottom-Up):** Iterative + Table filling (building the solution from the smallest base case up).
- [ ] **Classic Patterns:**
    - [ ] **1D DP:** Climbing Stairs, House Robber.
    - [ ] **2D DP (Grid):** Unique Paths, Minimum Path Sum.
    - [ ] **Knapsack Pattern:** 0/1 Knapsack, Unbounded Knapsack.
    - [ ] **String DP:** Longest Common Subsequence (LCS), Edit Distance.

---





## ⚡ Phase 6: Optimization Techniques (Problem Solving Patterns)
These are specific patterns frequently asked in coding interviews to optimize solutions.


**1. Two Pointers**
*Using two references (indices) to traverse data, typically to reduce nested loops.*
- [ ] **Opposite Ends (Meet in the Middle):**
    - [ ] **Scenario:** Sorted arrays.
    - [ ] **Logic:** Start `left=0`, `right=n-1`. Move them toward each other based on a condition.
    - [ ] **Classic Problem:** Two Sum II (Input array is sorted), Reverse a String, Valid Palindrome.
- [ ] **Same Direction (Fast & Slow / Read & Write):**
    - [ ] **Scenario:** Modifying an array in-place or detecting cycles.
    - [ ] **Logic:** `slow` pointer builds the valid data, `fast` pointer explores.
    - [ ] **Classic Problem:** Remove Duplicates from Sorted Array, Move Zeroes, Linked List Cycle Detection.
- [ ] **Merging Logic:**
    - [ ] **Scenario:** Comparing two separate lists.
    - [ ] **Classic Problem:** Merge Sorted Array, Intersection of Two Arrays.



**2. Sliding Window**
*Maintaining a subset of elements (a "window") that moves across the data structure.*
- [ ] **Fixed Size Window:**
    - [ ] **Logic:** Window size `k` is constant. Slide one step: remove element entering from left, add element entering from right.
    - [ ] **Classic Problem:** Maximum Sum Subarray of size K, Find all Anagrams in a string.
- [ ] **Dynamic / Variable Size Window:**
    - [ ] **Logic:** Expand the window (`right++`) until a condition breaks, then shrink the window (`left++`) until valid again.
    - [ ] **Classic Problem:** Longest Substring Without Repeating Characters, Minimum Window Substring, Longest Subarray with sum $\le$ K.
- [ ] **Auxiliary Data:** Using a Hash Map or Set inside the window to track frequencies.



**3. Prefix / Suffix Sums**
*Pre-computing cumulative totals to answer range queries in $O(1)$ time.*
- [ ] **1D Prefix Sum:**
    - [ ] **Concept:** Create array `P` where `P[i] = A[0] + ... + A[i]`.
    - [ ] **Query Formula:** Sum from `L` to `R` = `P[R] - P[L-1]`.
    - [ ] **Classic Problem:** Range Sum Query (Immutable), Find the Pivot Index.
- [ ] **Suffix Sum:**
    - [ ] **Concept:** Cumulative sum starting from the *end* of the array.
    - [ ] **Classic Problem:** Product of Array Except Self.
- [ ] **2D Prefix Sum:**
    - [ ] **Concept:** Pre-computing sums for sub-matrices.
    - [ ] **Classic Problem:** Matrix Block Sum, Range Sum Query 2D.
- [ ] **Difference Array:**
    - [ ] **Concept:** efficient range updates (adding X to indices L through R).



### 💡 Pattern Recognition Cheat Sheet

* **Sorted Array + Target Value?**  Try **Two Pointers**.
* **Subarray / Substring problem?**  Try **Sliding Window**.
* **Range Queries (Sum of index i to j)?**  Try **Prefix Sums**.
* **Cycle detection?**  Try **Fast & Slow Pointers**.





### 💼 Phase 7: Interview Preparation & Complexity Analysis

**1. Strategic Problem Solving (The "Grind")**
*Don't just solve random problems; solve patterns.*
- [ ] **LeetCode / HackerRank:**
    - [ ] **Blind 75 / NeetCode 150:** Focus on these curated lists. They cover 90% of interview patterns.
    - [ ] **Frequency:** Solve 1-2 problems daily. Consistency > Intensity.
    - [ ] **Topic-wise vs. Random:** Start topic-wise (e.g., 10 Array problems), then switch to "Random" to simulate real interviews.
- [ ] **CodeForces / CodeChef (Optional):**
    - [ ] Good for improving speed and handling edge cases, but often harder than standard job interviews.
- [ ] **The "15-Minute Rule":** If you are stuck for 15 minutes without an idea, look at the solution logic (not the code), understand it, close it, and try to write it yourself.

**2. Time Complexity Analysis (Master List)**
*You must be able to state the complexity of your code immediately after writing it.*

**A. The Three Asymptotic Notations**
- [ ] **Big O Notation ($O$) - Upper Bound (Worst Case)**
    - "The algorithm will never take longer than this."
    - Used to guarantee performance limits (e.g., "This sort takes at most $O(N^2)$").
- [ ] **Big Omega Notation ($\Omega$) - Lower Bound (Best Case)**
    - "The algorithm will never be faster than this."
    - Example: The best case for Bubble Sort is $\Omega(N)$ (already sorted).
- [ ] **Big Theta Notation ($\Theta$) - Tight Bound (Average Case)**
    - "The algorithm typically runs exactly like this."
    - Used when the Best and Worst cases are roughly the same complexity.


**B. Complexity Hierarchy (Fastest to Slowest)**
*Memorize this order. If your solution is lower on this list than the expected solution, you will likely get a "Time Limit Exceeded" (TLE).*

| Notation | Name | Example Algorithms |
| :--- | :--- | :--- |
| **$O(1)$** | **Constant** | Accessing Array Index, Hash Map Lookup |
| **$O(\log N)$** | **Logarithmic** | Binary Search |
| **$O(\sqrt{N})$** | **Square Root** | Prime Factors, Two Crystal Balls |
| **$O(N)$** | **Linear** | Looping through an array, Linear Search |
| **$O(N \log N)$** | **Linearithmic** | Merge Sort, Heap Sort, Quick Sort |
| **$O(N^2)$** | **Quadratic** | Nested Loops, Bubble/Insertion Sort |
| **$O(N^3)$** | **Cubic** | 3 Nested Loops, Matrix Multiplication |
| **$O(2^N)$** | **Exponential** | Recursion (Fibonacci), Power Set |
| **$O(N!)$** | **Factorial** | Permutations, Traveling Salesman Problem |

**C. Case Analysis**
- [ ] **Best Case:** The ideal input (e.g., Sorting an already sorted array). *Rarely used.*
- [ ] **Average Case:** Random input. *The most practical metric.*
- [ ] **Worst Case:** The "Killer" input. *Critical for stability guarantees.*

**3. Space Complexity Analysis**
*Often neglected, but critical for "Optimization" questions.*
- [ ] **Auxiliary Space:** Extra memory you use (Arrays, Hash Maps).
- [ ] **Stack Space:** Memory used by recursion (Call Stack).
- [ ] **In-Place Algorithms:** Algorithms that use $O(1)$ extra space (modifying the input array directly).

**4. Mock Interviews**
*Coding on a whiteboard/Google Doc is very different from an IDE with auto-complete.*
- [ ] **Behavioral Round:**
    - [ ] **STAR Method:** Situation, Task, Action, Result (for "Tell me about a time..." questions).
    - [ ] Prepare an "Elevator Pitch" (Introduction).
- [ ] **Technical Mock Rounds:**
    - [ ] **Pramp / Interviewing.io:** Platforms to practice with peers or engineers.
    - [ ] **"Rubber Duck" Debugging:** Explain your code out loud line-by-line.
    - [ ] **Whiteboard Coding:** Practice writing code without syntax highlighting.
     

My job is to **turn every empty checkbox in that README into a filled one** by writing code and solving problems. 🚀
