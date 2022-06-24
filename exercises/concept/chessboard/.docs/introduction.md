# Introduction

## Ranges

Ranges represent a sequence of one or many consecutive integers. They are created by connecting two integers with `..`.

``` elixir
1..5
```

Ranges can be ascending or descending. They are always inclusive of the first and last values.

A range implements the *Enumerable protocol*, which means functions in the `Enum` module can be used to work with ranges.
