# Dijkstra's Algorithm in C

## Overview

This project implements Dijkstra's algorithm to find the shortest paths from a starting node to all other nodes in a weighted graph. The graph is represented using an adjacency matrix. The program is written in C.

## Files

- `main.c`: Contains the main function and the implementation of Dijkstra's algorithm.


### Program Execution Flow

1. The program prompts the user to enter the number of vertices in the graph.
2. The user inputs the adjacency matrix, representing the weights of edges between vertices.
3. The user specifies the starting node from which the shortest paths are calculated.
4. The program outputs the shortest distance from the starting node to each other node and the corresponding path.

## Functions

### `int main()`

- **Purpose**: Initializes the graph, takes input from the user, and calls the `dijkstra` function to calculate the shortest paths.
- **Inputs**:
  - `n` (int): Number of vertices in the graph.
  - `G[MAX][MAX]` (int): Adjacency matrix representing the graph. `G[i][j]` is the weight of the edge from node `i` to node `j`. A value of `0` indicates no direct edge between the nodes.
  - `u` (int): The starting node for Dijkstra's algorithm.
- **Outputs**: None. The function outputs are handled within the `dijkstra` function.

### `void dijkstra(int G[MAX][MAX], int n, int startnode)`

- **Purpose**: Implements Dijkstra's algorithm to find the shortest path from the `startnode` to all other nodes in the graph.

- **Parameters**:
  - `G[MAX][MAX]` (int): The adjacency matrix of the graph.
  - `n` (int): The number of vertices in the graph.
  - `startnode` (int): The node from which the shortest paths are calculated.

- **Local Variables**:
  - `cost[MAX][MAX]` (int): A matrix that stores the cost of reaching each node.
  - `distance[MAX]` (int): Array that holds the shortest distance from the `startnode` to each other node.
  - `pred[MAX]` (int): Array that stores the predecessor of each node in the shortest path.
  - `visited[MAX]` (int): Array that indicates whether a node has been visited.
  - `count` (int): Counts the number of nodes seen so far.
  - `mindistance` (int): The minimum distance found in the current step.
  - `nextnode` (int): The next node to process, based on the minimum distance.

- **Description**:
  - The function initializes the `cost` matrix, setting the cost to `INFINITY` for nodes that are not directly connected.
  - It initializes the `distance` and `pred` arrays based on the starting node and sets the `visited` array to mark all nodes as unvisited initially.
  - The algorithm iteratively finds the next closest unvisited node, updates the shortest path estimates, and marks nodes as visited until all nodes have been processed.
  - Finally, the function outputs the shortest distances from the starting node to all other nodes and the corresponding paths.

- **Output**: Prints the shortest distance and the path from the starting node to each other node.

## Example Usage

When prompted, enter the number of vertices, the adjacency matrix, and the starting node. The program will then display the shortest distances and paths.

