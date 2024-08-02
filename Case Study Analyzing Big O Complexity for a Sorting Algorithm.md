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
Simply going line by line of the function:
Decalring a variable is negligible.
We then have a loop which is the first significant piece of code.
Immediately in the first loop, we have another loop which suggests a quadratic complexity. However a key componenet of this loop is that as this runs, its range decreases.
We have an if statemnt which will run on every single loop which also performs a simple math operation.
Two array position values are set.

In this case, the key operations which will contribute to time complexity are the nested loops.

## Task 2: Calculating Big O Complexity
The first loop is considered O(n).
The second loop decreases in range every loop, so we take the average time of this loop as O((n(n+1))/2).
Every other operation can be considered O(1), so negligible in complexity calculations.
This leaves us with O((n(n(n+1))/2)).


## Task 3: Efficiency Analysis:
We could always use the built in sort() function.
Besides that, an alternate way which should be faster is if we loop over every value in the as we do in the first loop here, but we have a new Linked List into which the value is inserted. We will loop over this new Linked list until we find a spot in which the next number is larger than the one we are trying to insert, and place the current number there. This should reduce O time to be O(log n).