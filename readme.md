# SLE-2: Empirical Performance Analysis of BFS and DFS

## Student Details

**Name:** Sanika Sudhakar Tavate
**PRN:** 25UAM128
**Course:** Introduction to Artificial Intelligence
**Course Code:** 02AML204
**Program:** SY B.Tech. CSE (AI & ML)\


---

## Experiment

**SLE-2 – Profiling Report (Empirical Performance Analysis)**

## Topic

**Performance Comparison of Breadth First Search (BFS) and Depth First Search (DFS)**

---

## 1. Objective

The objective of this experiment is to compare the empirical performance of BFS and DFS using:

- Execution time
- Number of nodes expanded
- Different search cases
- Py-Spy profiling

The same graph and search problem are used for both algorithms.

---

## 2. Algorithms Used

### Breadth First Search (BFS)

BFS explores the graph level by level using a queue.

### Depth First Search (DFS)

DFS explores one branch deeply before backtracking using a stack.

---

## 3. Graph Used

The experiment uses a small graph containing nodes from **A to Z**.

The starting node is:

**A**

Different goal nodes are used for different cases:

- Best Case → B
- Average Case → M
- Worst Case → Z

---

## 4. Cases Tested

| Case         | Start | Goal |
| ------------ | ----- | ---- |
| Best Case    | A     | B    |
| Average Case | A     | M    |
| Worst Case   | A     | Z    |

Each algorithm was executed **3 times** for every case.

---

## 5. Performance Metrics

The following metrics were measured:

1. Average execution time in milliseconds
2. Number of nodes expanded

Python's `time.perf_counter()` was used to measure execution time.

Py-Spy was also used as an additional profiling tool.

---

## 6. Experimental Results

| Case    | Algorithm | Nodes Expanded | Average Time (ms) |
| ------- | --------- | -------------: | ----------------: |
| Best    | BFS       |              2 |           0.00527 |
| Best    | DFS       |              2 |           0.00253 |
| Average | BFS       |             13 |           0.00833 |
| Average | DFS       |             22 |           0.01127 |
| Worst   | BFS       |             26 |           0.01127 |
| Worst   | DFS       |             23 |           0.01057 |

---

## 7. Search Paths

### Best Case

BFS:

`A → B`

DFS:

`A → B`

### Average Case

BFS:

`A → C → F → M`

DFS:

`A → C → F → M`

### Worst Case

BFS:

`A → C → F → M → Z`

DFS:

`A → C → F → M → Z`

---

## 8. Profiling Using Py-Spy

Py-Spy was used as an additional profiling tool to observe the runtime behavior of the Python search program.

A profiling file named:

`profile.svg`

was generated using Py-Spy.

The profiling program repeatedly executes BFS and DFS so that Py-Spy can collect sufficient samples.

---

## 9. Observation

The experiment was performed using the same graph for BFS and DFS.

In the best case, both algorithms expanded 2 nodes.

In the average case, BFS expanded 13 nodes while DFS expanded 22 nodes.

In the worst case, BFS expanded 26 nodes while DFS expanded 23 nodes.

The execution times were very small because the graph used in the experiment is small. Therefore, node expansion provides a useful additional metric for comparing the two algorithms.

---

## 10. Tools Used

- Python
- `time.perf_counter()`
- Py-Spy
- PowerShell
- GitHub

---

## 11. Files in This Project

```text
SLE2_IAI/
│
├── bfs_dfs.py
├── profile_search.py
├── profile.svg
├── README.md
└── CONTRIBUTION.md
```

---

## 12. Conclusion

BFS and DFS were implemented and tested on the same graph under best, average, and worst search cases. Execution time and nodes expanded were recorded for comparison. Py-Spy was additionally used to profile the search program. The experiment demonstrates how empirical measurements can be used along with theoretical understanding to analyze search algorithms.
