How can we reduce nested loops in C?
You can transform a nested loop into something that doesn’t look like a nested loop.

For example, you can turn this:

```
for (int i = 0; i < N; ++i) { 
  for (int j = 0; j < M; ++j) { 
    // ... something 
  } 
} 
```

Into this:

```
for (int k = 0; k < N*M; ++k) { 
  // ... something 
} 
```

And, you might need a little bit of compensation code, so you can reconstruct whatever i and j were responsible for in the original loops:

```
for (int k = 0, i = 0, j = 0; k < N*M; ++k) { 
  // ... something 
 
  if (++j == M) { 
    j = 0; 
    ++i; 
  } 
} 
```

Have you actually helped anything? It’s still logically a nested loop, even if its structure doesn’t immediately betray that fact.

Unless you had good reasons for folding the loops together, such as increased micro-optimization opportunities, you’ve mostly just made the program more complicated.

I used to perform this sort of transformation, and other transformations such as loop unrolling, unroll-and-jam, loop interchange, etc. when it opened up opportunities for instruction level parallelism and vectorization.

But, without a specific goal like that in mind and a plausible path to achieve it, there may not be a point.

Reducing loop nests by flattening as I did above doesn’t eliminate the computation you needed to perform. “Less nesting” isn’t a meaningful end in its own right.

It’s a potential tool to reach some other goal.
