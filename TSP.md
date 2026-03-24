# Experiment 12(d): Travelling Salesman Problem (TSP)

## Aim
To write a Python program to find the shortest possible route that visits every city exactly once and returns to the starting point using the Travelling Salesman Problem (TSP) approach.

---

## Algorithm

1. **Input the Number of Cities**:
   - Begin by taking the number of cities as input.
   
2. **Distance Matrix**:# Ex. No: 18D - Travelling Salesman Problem (TSP)

## AIM:
To write a Python program to find the shortest possible route that visits every city exactly once and returns to the starting point using the **Travelling Salesman Problem (TSP)** approach.

## ALGORITHM:

**Step 1**: Start the program.

**Step 2**: Input the number of cities and the distance matrix.

**Step 3**: Set the starting city (e.g., city `0`).

**Step 4**: Generate all possible permutations of the remaining cities.

**Step 5**: For each permutation:
- Calculate the total cost of traveling through the permutation starting and ending at city `0`.
- Keep track of the **minimum cost** and the corresponding route.

**Step 6**: Return the **route** and the **minimum cost**.

**Step 7**: End the program.

## PYTHON PROGRAM

```python
from sys import maxsize
from itertools import permutations
V = 4
def travellingSalesmanProblem(graph, s):
    vertex = []
    for i in range(V):
        if i != s:
            vertex.append(i)
    min_path = maxsize
    next_permutation = permutations(vertex)
    for perm in next_permutation:
        current_pathweight = 0
        k = s
        for j in perm:
            current_pathweight += graph[k][j]
            k = j
        current_pathweight += graph[k][s]
        min_path = min(min_path, current_pathweight)
    return min_path
if __name__ == "__main__":
    graph = [[0, 10, 15, 20],
             [10, 0, 35, 25],
             [15, 35, 0, 30],
             [20, 25, 30, 0]]
    s = int(input())
    print(travellingSalesmanProblem(graph, s))
```

## OUTPUT
<img width="1185" height="198" alt="image" src="https://github.com/user-attachments/assets/86f36feb-a31b-4f64-b947-ad20cea3891b" />

##RESULT
Therefore, the output is the example to write a Python program to find the shortest possible route that visits every city exactly once and returns to the starting point using the **Travelling Salesman Problem (TSP)** approach.

   - Define the distance matrix where each element `graph[i][j]` represents the distance between city `i` and city `j`.

3. **Generate All Permutations**:
   - Generate all possible permutations of the cities excluding the starting city.
   
4. **Calculate the Total Cost for Each Permutation**:
   - For each permutation, calculate the total distance of traveling through the cities in that order, starting and ending at the initial city.
   
5. **Track the Minimum Cost**:
   - Keep track of the minimum cost and the corresponding route.

6. **Return the Best Route and Minimum Cost**:
   - Once all permutations are evaluated, return the route with the minimum cost.

7. **End the Program**:
   - Output the minimum cost and the corresponding route.

---

## Program
```

```

## OUTPUT


## RESULT
