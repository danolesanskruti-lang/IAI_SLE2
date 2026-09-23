# SLE-2: Empirical Performance Analysis — BFS vs DFS

**Course:** 02AML204 – Introduction to Artificial Intelligence  
**Student:** Sanskruti Sandeep Danole  
**PRN:** 25UAM059  
**Division:** A  
**Repository:** IAI_SLE2

## 1. Objective
This SLE-2 experiment compares **Breadth-First Search (BFS)** and **Depth-First Search (DFS)** on the same 20-node graph, using the same start node (A) and goal node (T). The purpose is to measure actual execution performance rather than only discuss theory.

## 2. Algorithms Profiled
- Algorithm A: Breadth-First Search (BFS)
- Algorithm B: Depth-First Search (DFS)
- Problem: 20-node graph search from A to T
- Implementation: Python
- Node metric: number of nodes expanded before reaching the goal

## 3. Profiling Method
The program in `bfs_dfs.py` runs BFS and DFS on exactly the same graph, repeats each search 10,000 times so timing differences are measurable, counts expanded nodes, and uses `perf_counter()` for total and average execution time.

### py-spy
Run a flame-graph profile with:

    py-spy record -o bfs_dfs.svg -- python bfs_dfs.py

For a live view:

    py-spy top -- python bfs_dfs.py

The py-spy commands are the profiling procedure. Run them on your own computer and keep the generated SVG/screenshot as evidence if required.

## 4. Results
Run `python bfs_dfs.py`. The program prints the actual measured values for your computer. Record those values in the SLE-2 Word report. Do not copy numbers from another computer.

| Metric | BFS | DFS |
|---|---:|---:|
| Nodes expanded | Run result | Run result |
| Total time for 10,000 runs (ms) | Run result | Run result |
| Average time per run (ms) | Run result | Run result |

Expected path with the current neighbour ordering: `A → C → F → L → T`.

## 5. Comparison and Analysis
The final comparison should be based on the measured numbers. Lower measured average time means lower execution time for this particular experiment. Node count shows how much of the graph each algorithm explored before reaching the goal.

The result depends on the graph structure and search order, so report it as an empirical result for this test case rather than claiming that one algorithm is always faster. For larger graphs, BFS can require substantial frontier memory, while DFS generally uses less frontier memory but does not guarantee a shortest path.

## 6. AI Contribution Log
| Activity | Contribution |
|---|---|
| Problem selection | Selected BFS vs DFS because it is one of the recommended SLE-2 comparison pairs. |
| Code development | AI assistance was used to draft and organize the Python BFS/DFS experiment. |
| Profiling setup | AI assistance was used to prepare the timing benchmark and py-spy commands. |
| README/report structure | AI assistance was used to structure the README according to the SLE-2 guideline. |
| Experiment execution | Student should run the program and py-spy on her own system and record actual values. |
| Interpretation | Student should compare measured numbers and write final justification from observed data. |

## 7. Files
- `bfs_dfs.py` — BFS/DFS implementation, node counter and timing benchmark.
- `README.md` — SLE-2 experiment description, profiling method and AI contribution log.

## 8. Conclusion
This experiment demonstrates how BFS and DFS can be compared using empirical measurements. Instead of relying only on theoretical complexity, it records execution time and nodes expanded for the same graph. The final conclusion should be based on the actual measurements collected on the student's computer.

**SLE-2 reminder:** The report should contain real numbers, a comparison table, data-based justification, and an honest AI contribution note.