# Loop with incrementation
``` Java
// loop with increment
for (int i=0 ; i<N ; ++i) {......}
 // or  
for (int i=0 ; i<=N-1 ; ++i) {......}
```
# Loop with decrementation
``` Java
// loop with decrement
for (int i = N ; i > 0 ; --i) {.....}
 // or 
for (int i = N-1 ; i >= 0 ; --i) {.....}

# other decrement

```

# Single LOOP 

``` Java
// This FOR loop can be optimised
for (int i=0 ; i<N ; ++i) {......}

 // or this 
for (int i=0 ; i<=N-1 ; ++i) {......}
 
 // can be transformed to 

for (int i = N ; i > 0 ; --i) {.....}

 // or to

for (int i = N-1 ; i >= 0 ; --i) {.....}

```

# Double Loop
If For has to be used twice for traversing an object or data structure, 
instead of using two For Loops with incrementation, it is useful to optimised 
one of the loops by using increment.

``` Java
// first increment
for (int i=0 ; i<M ; ++i) 
{
  // second increment
  for (int j=0 ; j<N ; ++j) 
  {
  ....................................
  }
}

# to be OPTIMISED

// first decrement
for (int i = M-1 ; i >=0 ; --i) 
{
  // second increment
  for (int j=0 ; j<N ; ++j) 
  {
  ....................................
  }
}

# Other OPTIMISATION

// first decrement
for (int i = M-1 ; i >=0 ; --i) 
{
  // second increment
  for (int j=0 ; j<N ; ++j) 
  {
  ....................................
  }
}

```








