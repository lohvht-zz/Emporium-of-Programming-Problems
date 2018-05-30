# Solutions to Array Problems
These are some sample solutions to the array problems in the main readme

## First Duplicate
Naive solution in Python3

```
def firstDuplicate(a):
  array2 = []
  for el in a:
    if el in array2:
      return el
    else:
      array2.append(el)
  return -1
```

<details>
<summary>Quicker Solution (without using extra memory)</summary>
<br>

In Python3
```
def firstDuplicate(a):
  for i in range(len(a)):
    index = abs(a[i]) - 1
    if a[index] < 0:
      return abs(a[i])
    else:
      a[index] = -a[index]
    return -1
```

This works as we take advantage of the guaranteed constraints provided in the
question, namely that the array only contains numbers in the range from 1 to
the array.length. Thus if we have already seen `a[i]` once, then the `a[index]`
where `index = abs(a[i]) - 1` would have been negative, thus showing that the
second occurence of `a[i]`
<details>

## First Non Repeating Character
<details>
<summary>Solution</summary>
<br>

In Python3
```
def firstNotRepeatingCharacter(s):
    alphabet_count_dict = {}
    string_order_dict = {}
    for i in range(len(s)):
        char = s[i]
        if char not in alphabet_count_dict:
            alphabet_count_dict[char] = 1
            string_order_dict[char] = i
        else:
            alphabet_count_dict[char] += 1
    min_order = sys.maxsize
    min_key = '_'
    for key, val in alphabet_count_dict.items():
        if val == 1 and min_order > string_order_dict[key]:
            min_order = string_order_dict[key]
            min_key = key
    return min_key
```
TODO: Find a solution that does not take extra space!!!
This solution utilises 2 additional dictionaries, 1 to count the number of
alphabets found in `s` (`alphabet_count_dict`), and 1 that keeps track of the
order of which character came first in `s` (`string_order_dict`).

If done on languages that are not on python or on strictly arrays, this can be
done with 2 alphabet-sized (length 26) arrays to keep track
<details>