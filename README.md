# Elixir Enum.each List Modification Bug

This repository demonstrates an unexpected behavior when modifying a list while iterating over it using `Enum.each` in Elixir.  Modifying the list in place within the loop does not affect the list being iterated over. The code attempts to remove the element `3` from the list, but the removal does not happen as expected.  The solution provides a correct approach to achieve the desired list modification.

**Bug:** The list modification occurs in an immutable way, leaving the original list untouched by the `List.delete` function inside the `Enum.each` loop.

**Solution:** Using `Enum.filter` offers a functional and correct way to remove the element from the list.