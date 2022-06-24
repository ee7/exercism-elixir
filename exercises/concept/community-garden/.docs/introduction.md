# Introduction

## Agent

The `Agent` module facilitates an abstraction for spawning [processes and the *receive-send* loop](https://exercism.org/tracks/elixir/concepts/processes). From here, we will call processes started using the `Agent` module *'agent processes'*. An *agent process* might be chosen to represent a central shared state.

To start an *agent process*, `Agent` provides the `start/2` function. The supplied function when `start`*-ing* the *agent process* returns the initial state of the process:

``` elixir
# Start an agent process with an initial value of an empty list
{:ok, agent_pid} = Agent.start(fn -> [] end)
```

Just like `Map` or `List`, `Agent` provides many functions for working with *agent processes*.

It is customary to organize and encapsulate all `Agent`-related functionality into a module for the domain being modeled.
