# Introduction

## Access Behaviour

Elixir uses code *Behaviours* to provide common generic interfaces while facilitating specific implementations for each module which implements it. One such common example is the *Access Behaviour*.

The *Access Behaviour* provides a common interface for retrieving data from a key-based data structure. The *Access Behaviour* is implemented for maps and keyword lists, but let's look at its use for maps to get a feel for it. *Access Behaviour* specifies that when you have a map, you may follow it with *square brackets* and then use the key to retrieve the value associated with that key.

``` elixir
# Suppose we have these two maps defined (note the difference in the key type)
my_map = %{key: "my value"}
your_map = %{"key" => "your value"}

# Obtain the value using the Access Behaviour
my_map[:key] == "my value"
your_map[:key] == nil
your_map["key"] == "your value"
```

If the key does not exist in the data structure, then `nil` is returned. This can be a source of unintended behavior, because it does not raise an error. Note that `nil` itself implements the Access Behaviour and always returns `nil` for any key.
