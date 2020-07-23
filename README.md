# M0_C8 - Intersection
Repository with prompt and code for Module 1, Challenge 8: Intersection.

## Prompt
You're a detective who's working on a series of criminal cases. You have a sneaking suspicion that a current case might be related to a cold case that happened 10 years ago.

Each crime has had all of its evidence and clues boiled down to a list of key terms. If both crimes have at least 3 elements in common, then you have enough evidence to re-open the cold case. If any crime scene has fewer than 3 pieces of evidence, then it's enough if all of their evidence matches.

**Be careful though!** Because some of the interns were careless, some of the crime scene reports have duplicate items. You'll have to account for that when comparing crime scenes and make sure not to double-count the same piece of evidence!

### Requirements

Write a function that checks for these overlaps.

- If there are at least 3 common pieces of evidence between both, return the `True` boolean. Otherwise, return `False`.
- If either list has fewer than 3 pieces of **effective** evidence, then all pieces of the evidence in the smaller crime must be found in the larger crime. For example, if one crime has only two elements, then both of those elements must be found in the other crime for the function to return `True`.
- The return values should be actual booleans, not strings.
- If there are duplicate items within one scene (or even both), they only count as one match. For example, the below two crimes only have one item in common (`kitchen`):

```
crime1: kitchen kitchen knife bathroom
crime2: kitchen veranda
```

### Assumptions
- The inputs will be two lists of strings.
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

In this example, the first crime again only has two items. However, only one of those elements intersects with the second crime, so the function returns `False`.

## Example 4
```
$ python3 intersection.py
crime1: knife ruler knife
crime2: garage car wrench ruler ruler knife
False
```

The above example only has 2 effective matches. `Knife` shows up twice in `crime1`, so `crime1` has effectively only 2 items. `ruler` shows up in `crime2` twice, so it effectively has 5 items, not 6.

Since `crime1` is effectively 2 items and both items are found in `crime2`, the function will return `True`.

## Notes and Hints
- Remember to handle duplicates! There's a nice little function for that...

## Knowledge Tested
- Conditionals
- Loops
- Sets
- Lists

## Instructions
1. Fork this repository to your own account.
2. Clone the forked repository to your local computer.
3. Inside `intersection.py`, you will implement your code. You should only modify the function `check_overlap(crime1, crime2)` and nothing else. 
4. While you're writing and/or when you're done, you can execute the provided tests to verify your program works by running `python3 test_intersection.py`. All tests are passing if you see `OK` in the output.
