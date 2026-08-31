# Task 008 — Arrays and tuples

**Concept:** `T[]` is a variable-length list of one type; a tuple (`[string, number]`) is a
fixed-length, fixed-order list of specific types per position — useful when a function needs to
return exactly two related-but-different values (like React's `useState` later returns).

**Step 1 — build it yourself, no AI:** type an array of `Product` (task 003), then write a
function `minMax(numbers: number[]): [number, number]` returning a tuple, destructure its result
into two named variables, and try assigning the tuple's two positions in the wrong order to see
the type error.

**Done when (step 1):** `minMax`'s return type is enforced as exactly two numbers in that order,
and swapping the destructuring order produces logically wrong (but type-valid) results you can
explain the difference between "type-correct" and "logically correct."

**Step 2 — AI review pass:** ask the AI for a real library function that returns a tuple (hint:
React's `useState`) and why a tuple was chosen over an object there.

**Stretch (optional):** add a named-tuple label (`[min: number, max: number]`) for readability.
