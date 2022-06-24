# Introduction

## Nil

[Nil](https://www.merriam-webster.com/dictionary/nil) is an English word meaning "nothing" or "zero". In Elixir, `nil` is a special value that means an *absence* of a value.

``` elixir
# I do not have a favorite color
favorite_color = nil
```

In other programming languages, `null` or `none` values might play a similar role.

## If

Besides `cond`, Elixir also provides the macro [`if/2`](https://elixir-lang.org/getting-started/case-cond-and-if.html#if-and-unless) which is useful when you need to check for only one condition.

[`if/2`](https://hexdocs.pm/elixir/Kernel.html#if/2) accepts a condition and two options. It returns the first option if the condition is *truthy*, and the second option if the condition is *falsy*.

``` elixir
age = 15

if age >= 16 do
  "You are allowed to drink beer in Germany."
else
  "No beer for you!"
end

# => "No beer for you!"
```

It is also possible to write an `if` expression on a single line. Note the comma after the condition.

``` elixir
if age > 16, do: "beer", else: "no beer"
```

This syntax is helpful for very short expressions, but should be avoided if the expression won't fit on a single line.

### *Truthy* and *falsy*

In Elixir, all datatypes evaluate to a *truthy* or *falsy* value when they are encountered in a boolean context (like an `if` expression). All data is considered *truthy* **except** for `false` and `nil`. In particular, empty strings, the integer `0`, and empty lists are all considered *truthy* in Elixir.
