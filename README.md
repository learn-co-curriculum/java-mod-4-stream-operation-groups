# Stream Operation Groups

## Learning Goals

- Identify and explain the two groups of stream operations
- Identify some of the operations in each group

## The Two Groups of Stream Operations

We can perform several operations on streams. These operations are divided into
two groups:

1. **Intermediate Operations:** These operations are evaluated lazily, i.e., not
   immediately, and always returns a new stream. These can be chained together
   to perform several intermediate operations before a terminal operation is
   executed.
2. **Terminal Operation:** These operations produce a result or side-effect from
   a stream. A stream can have only one terminal operation.

## Operations List

Here are a few intermediate and terminal operations. We’ll look at some these in
more detail in the following lessons.

**Intermediate Operations:**

- `map`: transforms each element in a given stream and returns a new stream
- `filter`: returns a new stream that only includes elements that return true
  for a given predicate function
- `distinct`: a new stream is returned with only unique elements
- `sorted`: sorts elements according to their natural order or a comparator

**Terminal Operations:**

- `max`: returns an Optional maximum element in the given stream according to a
  comparator
- `min`: returns an Optional minimum element in the given stream according to a
  comparator
- `count`: returns the total number of elements as a `long` type
- `forEach`: applies the given consumer to each element
- `reduce`: aggregates all the values in the stream into a single value
- `allMatch`: returns true if all elements match the given predicate
- `anyMatch`: returns true if a single element matches the given predicate
- `noneMatch`: returns true if no elements match the given predicate
- `toArray`: puts all the elements in an array and returns it
- `collect`: returns a collection of the values
