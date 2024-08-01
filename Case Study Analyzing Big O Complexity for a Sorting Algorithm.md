# Problem Statement: Consider a sorting algorithm that arranges an array of integers in ascending order. The challenge is to analyze the Big O complexity of the algorithm and assess its efficiency in various scenarios.

```
def simple_sort(arr):
    n = len(arr)
    for i in range(n):
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
```

## Task 1: Identifying Key Operations

## Task 2: Calculating Big O Complexity

## Task 3: Efficiency Analysis: