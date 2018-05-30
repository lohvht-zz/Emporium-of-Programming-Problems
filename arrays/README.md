# Array Problems
Problems that deal with arrays and array traversal. Questions with hints
that go with `Given an array that contains only numbers in the range from 1 to
array.length` usually has some in array properties that can be exploited

## First Duplicate
Given an array a that contains only numbers in the range from 1 to a.length,
find the first duplicate number for which the second occurrence has the minimal
index. In other words, if there are more than 1 duplicated numbers, return
the number for which the second occurrence has a smaller index than the second
occurrence of the other number does. If there are no such elements, return -1.

### Example
For `a =[2,1,3,5,3,2]`, the output should be `firstDuplicate(a) = 3`
Since there are 2 duplicates, `2`, and `3`, second occurence of `3` has smaller
index than second occurence of `2`, thus answer is 3.

For `a=[2,4,3,5,1]`, output should be `firstDuplicate(a)=-1`

### Input/Output
- [input] array.integer a
constraints: `1 ≤ a.length ≤ 100000`, `1 ≤ a[i] ≤ a.length`

- [output] integer

## First Non Repeating Character
Given a string s, find and return the first instance of a non-repeating
character in it. If there is no such character, return '_'.

Note: Write a solution that only iterates over the string once and uses O(1)
additional memory, since this is what you would be asked to do during a real
interview.

### Example
For `s = "abacabad"`, the output should be `firstNotRepeatingCharacter(s) = 'c'.`
There are 2 non-repeating characters in the string: `'c'` and `'d'`. Return `c`
since it appears in the string first.

For `s = "abacabaabacaba"`, the output should be
`firstNotRepeatingCharacter(s) = '_'`.
There are no characters in this string that do not repeat.

### Input/Output
- [input] string s
A string that contains only lowercase English letters.
constraints: `1 ≤ s.length ≤ 105`

- [output] char
The first non-repeating character in `s`, or `'_'` if there are no characters
that do not repeat.