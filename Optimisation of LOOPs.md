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
// other decrement
for (int i = N ; --i >= 0 ;) {.....}

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

 // other decrement
 
for (int i = N ; --i >= 0 ;) {.....}

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

# ... to be OPTIMISED

// first decrement
for (int i = M-1 ; i >=0 ; --i) // for (int i = M ; --i >= 0 ;)
{
  // second increment
  for (int j=0 ; j<N ; ++j) 
  {
  ....................................
  }
}

# Other OPTIMISATIONS

// // N° 1
// first decrement
for (int i = M ; --i >= 0 ;)
{
  // second increment
  for (int j=0 ; j<N ; ++j) 
  {
  ....................................
  }
}

// // N°2

//You may omit any of the three exprs in the for loop header

int value;
int incrementAmount;

for ( ; startingvalue <= 100; )
{
 startingvalue = startingvalue + incrementAmount;
}
// technically it’s a count controlled loop, but use a while

```
# Pre-incrementation and Post-incrementation

```Java
# Post-Incre/Decre/mentation
num++; //equivalent to: num = num + 1;
num--; //equivalent to: num = num - 1;

# Pre-Incre/Decre/mentation
++num; //equivalent to: num = num + 1;
--num; //equivalent to: num = num - 1;

```

# Explanations to be found here

 - [https://www.netjstech.com/2019/06/java-for-loop-with-examples.html](https://www.netjstech.com/2019/06/java-for-loop-with-examples.html)
 - [https://www.geeksforgeeks.org/practice-questions-time-complexity-analysis/](https://www.geeksforgeeks.org/practice-questions-time-complexity-analysis/)
 - [https://www.geeksforgeeks.org/analysis-of-algorithms-set-4-analysis-of-loops/](https://www.geeksforgeeks.org/analysis-of-algorithms-set-4-analysis-of-loops/)
 - [https://www.baeldung.com/java-algorithm-complexity](https://www.baeldung.com/java-algorithm-complexity)
 - 
