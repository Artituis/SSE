# 1

## a) Name the three types of graphs that are combined into a Code Property Graph (CPG). For each, briefly state what it captures that the previous one cannot.

### Abstract Syntax Tree (AST)

- Describes program structure

- Enables pattern matching

- Language Agnostic

- Doesn't show execution order

- Can't tell reacheble paths to sinks

### Control Flow Graphs (CFG)

- Shows execution order

- Show all possible execution sequences

- Doesn't show data dependecies 

- Doesn't show what data reaches the sink

### Program Dependence Graphs (PDG)

- Shows the path that the data took, from source to sink



## b) What is the difference between SAST and DAST? Name one advantage and one disadvantage of each.
SAST analyses code without running it. might have higher false positives. and does not analyses dinamic features and problems
DAST lower false positives. may not go through all code paths. and might not have a defined end ( it needs to be defined by the coder)
## c) Explain what fuzzing is and what the two main components of a fuzzer are.
fuzzing generates mutated and random data to test the system

imput generation

bug detection and observation
se the control/data path


know how to work with code property graphs
