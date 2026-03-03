# Pacman-Pathfinding-Algorithms-Showcase
Showcase summary of my Pacman Search Algorithms Project, including DFS, BFS, UCS, A*, heuristics, and suboptimal search. (No source code due to academic policy.)

# Pacman-Search-Project-Showcase

This is a **showcase version only**.  
Full source code is intentionally **not included** to comply with university academic policy.

---

## Overview
In this project, I implemented several foundational AI search algorithms and applied them to the Pacman environment. The goal was to design agents that navigate mazes, reach goals efficiently, and collect food while minimizing cost.

I implemented:
- Depth-First Search (DFS)
- Breadth-First Search (BFS)
- Uniform Cost Search (UCS)
- A* Search with heuristics
- Corners Problem + Heuristic
- Food Search Problem + Heuristic
- Closest Dot Search

All algorithms were written by me and passed every autograder test with full marks.

---

## Key Components I Implemented

### **Depth-First Search (DFS)**
- Implemented graph-based DFS using a stack.  
- Avoided revisiting explored states for correctness.  
- Returned valid action sequences for multiple maze layouts.  

### **Breadth-First Search (BFS)**
- Implemented BFS using a queue for shallowest-node expansion.  
- Guaranteed shortest paths by number of actions.  
- Used BFS for PositionSearch and AnyFoodSearchProblem.  

### **Uniform Cost Search (UCS)**
- Used a priority queue to expand nodes by increasing cost.  
- Tracked best-known path costs to avoid unnecessary expansions.  
- Enabled custom cost functions (StayEast, StayWest).  

### **A* Search**
- Implemented full A* with `f(n) = g(n) + h(n)` logic.  
- Supported multiple heuristics including Manhattan distance.  
- Achieved faster optimal solutions than UCS on large maps.

---

## Corners Problem

### **Custom State Representation**
- Designed a state structure storing Pacman’s position and visited corners.  
- Ensured independence between states for correct graph search behavior.

### **Successor Function**
- Generated legal moves and updated visited corner status.  
- Assigned uniform step cost of 1.

### **Corners Heuristic**
- Created an admissible, non-trivial heuristic.  
- Used distances to unvisited corners to reduce node expansions.  
- Passed all autograder thresholds.

---

## Food Search Problem

### **A* Food Heuristic**
- Developed a non-trivial heuristic combining:  
  - Nearest food distance  
  - Maze spread (food cluster estimation)  
- Significantly reduced expanded nodes (far below the 15k requirement).  
- Achieved full credit on the autograder.

---

## Closest Dot Search

### **AnyFoodSearchProblem**
- Added goal test to detect any food location.  

### **findPathToClosestDot**
- Implemented BFS-based solution to reach the nearest dot.  
- Used inside `ClosestDotSearchAgent` to quickly produce suboptimal but efficient paths.

---

## GenAI Learning & Workflow Integration

Throughout this project, I used GenAI tools such as **Claude** and **Code Interpreter models** to support (but not generate) my work. These tools helped me:

### **Debug Faster**
- Analyzed stack traces and logic errors.  
- Identified incorrect state transitions or inconsistent cost tracking.

### **Understand Multi-File Interactions**
- Clarified how `search.py`, `searchAgents.py`, and the Pacman engine connect.  
- Helped me conceptualize data flow without revealing project solutions.

### **Improve Code Structure**
- Translated rough pseudocode into clearer templates that I then implemented myself.  
- Reinforced clean design of queues, priority queues, and visited sets.

### **Explore Heuristic Behavior**
- Used AI explanations to compare different heuristic strategies.  
- Ensured heuristics remained admissible and consistent.

### **Strengthen AI Engineering Skills**
This project deepened my understanding of:
- Classical search algorithms  
- Pathfinding  
- Heuristics design  
- Multi-agent reasoning  
- How AI tools can complement engineering workflows safely and responsibly

---
