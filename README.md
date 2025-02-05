# Elixir Bug: Modifying a List During Enum.each Iteration

This repository demonstrates a common error in Elixir when attempting to modify a list while iterating over it using `Enum.each`.  The provided code intends to remove the element `3` from the list, but due to Elixir's immutability, the modification is not reflected in the original list. The solution demonstrates how to correctly handle such scenarios.

## Bug
The `bug.exs` file contains the erroneous code. The `Enum.each` loop does not modify the original list because Elixir uses immutable data structures. The `List.delete` function creates a new list instead of modifying the existing one.