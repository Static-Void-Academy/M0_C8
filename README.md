# M0_C8 - Intersection
Repository with prompt and code for Module 1, Challenge 8: Intersection.

## Prompt
You're a detective who's working on a series of criminal cases. You have a sneaking suspicion that a current case might be related to a cold case that happened 10 years ago.

Each crime has had all of its evidence and clues boiled down to a list of key terms. If both crimes have at least 3 elements in common, then you have enough evidence to re-open the cold case. If any crime scene has fewer than 3 pieces of evidence, then it's enough if all of their evidence matches.

### Requirements

Write a function that checks for these overlaps.

- If there are at least 3 common pieces of evidence, return the `True` boolean. Otherwise, return `False`.
- If either list has fewer than 3 pieces of evidence, then all pieces of the evidence must match. For example, if `crime1` has only two elements, then both of those elements must be found in `crime2` for the function to return `True`.
- The return values should be actual booleans, not strings.

### Assumptions
- The inputs will be two lists of strings.
- There will be no duplicate words within one list.
- There will be no empty lists.

The main function has been written for you so you can test your own space-delimited lists of words.

## Example 1
```
$ python3 intersection.py
crime1: bed windows carpet chandelier
crime2: windows carpet veranda porch backyard
False
```

In this example, you can see that there were two items in common: "windows" and "carpet". However, this does not meet the minimum threshold of three, and both lists have more than three elements.

## Example 2
```
$ python3 intersection.py
crime1: drapes computer
crime2: kitchen knife computer sink bathroom drapes
True
```

In this example, `crime1` has only two items. Both items were found in `crime2`, so this returns as `True`.

## Example 3
```
$ python3 intersection.py
crime1: knife ruler
crime2: garage car wrench knife
False
```

In this final example, the first crime again only has two items. However, only one of those elements intersects with the second crime, so the function returns `False`.

## Notes and Hints
- It doesn't matter how you solve this as long as you use a set as your data structure.

## Knowledge Tested
- Conditionals
- Loops
- Sets

## Instructions
1. Fork this repository to your own account.
2. Clone the forked repository to your local computer.
3. Inside `intersection.py`, you will implement your code. You should only modify the function `check_overlap(crime1, crime2)` and nothing else. 
4. While you're writing and/or when you're done, you can execute the provided tests to verify your program works by running `python3 test_intersection.py`. All tests are passing if you see `OK` in the output.
