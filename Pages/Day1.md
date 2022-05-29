# Day 1 - Sunday, May 29th. 2022

## The story attached to the pain of growth for me:

1. What’s your perspective?
    - That this is **necassary**.  
2. Why are you doing this?
    - To change and to be free.
3. Do you want what comes at the end of this journey?
    - I am tempted to believe so. However, I've learned to brace for the worst while looking forward to the best, so basically; **we'll see : )** .
4. Are you doing this for you?
    - Mainly, **yes**.


## Big O Notation:
- **O(1)** describes an algorithm that will always execute in the same time (or space) regardless of the size of the input data set. [(1)][1]
- **O(N)** describes an algorithm whose performance will grow linearly and in direct proportion to the size of the input data set. [(1)][1]
 
  > 'Big O favors the worst-case performance scenario; a condition could be met during any iteration of a for loop and the function would return early, but Big O notation will always assume the upper limit where the algorithm will perform the maximum number of iterations.' [(2)][2]

- **O(N²)** represents an algorithm whose performance is directly proportional to the square of the size of the input data set. [(1)][1]
 
- **O(2^N)** denotes an algorithm whose growth doubles with each addition to the input data set. [(1)][1]

  > '_**Binary search**_ is a technique used to search sorted data sets. It works by selecting the middle element of the data set, essentially the median, and compares it against a target value... It will continue to halve the data set with each iteration until the value has been found or until it can no longer split the data set. [(2)][2]
  
  >**This type of algorithm is described as O(log N).** The iterative halving of data sets described in the binary search example produces a growth curve that peaks at the beginning and slowly flattens out as the size of the data sets increase' [(2)][2]

<br/>

## Mutable and immutable objects
Mutable and immutable objects are handled differently in python. Immutable objects are quicker to access and are expensive to change because it involves the creation of a copy.
Whereas mutable objects are easy to change.
Use of mutable objects is recommended when there is a need to change the size or content of the object.

The difference could be summerised by saying that **immutable** and **mutable** objects are no different from one another in the way they are assigned, but rather in the way they are '_changed'_, meaning that while ***mutable** objects (i.e. lists, ets.) can be mutated permanently*,  
*changing an **immutable** object (i.e. int., strings, etc.) is just rebinding the name assigned to it*.

## Hexspeak 
Hexspeak, like leetspeak, is a novelty form of variant English spelling using the hexadecimal digits. Created by programmers as memorable magic numbers, hexspeak words can serve as a clear and unique identifier with which to mark memory or data. [wikipedia][3]
### For fun, check this [List](https://gist.github.com/gabrielfalcao/c942f6602401f0697c206e30f0aa4bad?permalink_comment_id=2737669) on GitHub.

<br/>

## Things I want to know more about
- Scopes.
- Data  Flow.
- `return` in Python.




[1]: https://rob-bell.net/2009/06/a-beginners-guide-to-big-o-notation
[2]: https://rob-bell.net/2009/06/a-beginners-guide-to-big-o-notation
[3]: https://en.wikipedia.org/wiki/Hexspeak