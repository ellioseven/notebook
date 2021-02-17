# Cracking the Code Interview



## Cracking the Code Interview

### Big O

* A way to determine efficiency of an algorithm, describes the rate of increase
* Example:
  * The runtime of electronic file transfer is O\(s\), where s is the size of a file, meaning the time increases linearly as the file increases
  * The runtime of airplane transfer is O\(1\), the time is constant, meaning that the time will be the same no matter the file size
* Time/Space forms \(see fig-1.png\):
  * O\(log n\)
  * O\(n log n\): Decreases by a fraction of 2
  * O\(n\): Increases linear to input size
  * O\(n^2\): Increaes by a multiple of 2
  * O\(2^n\)
* Drop constants, as time may different on the size of the inputs
* Drop non dominant terms, eg: N^2 + N becomes N&2
* See fig-2.png for example of adding vs multiplying runtimes
* Recursive runtime: @todo

#### Examples

@todo

### Technical Questions

* Practice solving coding problems on paper
* See \(fig-3.png\) for a table of must have data structure and algorithm knowledge

#### Problem Solving Approach

* See fig-4.png for a problm solving flow chart
* Listen carefully
  * Most of the time information is there for a reason
  * Consider rewriting important information
  * Make sure you record any unique information
    * "Given two arrays that are sorted...": Why are they sorted?
    * "Design an algorithm to be run repeatly on a server...": What would they be looking for? Caching?
  * If you're stuck, asking yourself if you've used all the information
* Draw an example
  * Always draw an example, it will give you more insight than working it out inside your head
  * Example should be:
    * Specific: Use real values
    * Sufficiently large: Use a large amount of values
    * Not a special case
* State a brute force
  * 

