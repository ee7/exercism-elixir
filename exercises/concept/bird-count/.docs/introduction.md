# Introduction

## Recursion

Recursive functions are functions that call themselves.

A recursive function needs to have at least one *base case* and at least one *recursive case*.

A *base case* returns a value without calling the function again. A *recursive case* calls the function again, modifying the input so that it will at some point match the base case.

Very often, each case is written in its own function clause.

``` elixir
# base case
def count([]), do: 0

# recursive case
def count([_head | tail]), do: 1 + count(tail)
```
