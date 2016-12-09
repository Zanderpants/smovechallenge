# Booking Validation Problem
Unlike the other challenges, this one requires you to programmatically solve a specific problem. 

You are given a set of data representing a sequence of bookings on a single car. Each booking consists of a start location and an end location. Given two adjacent bookings *b1* and *b2*, we say a *relocation* is required between those bookings if the end location of *b1* ≠ the start location of *b2*.

For example,

```
   b1        b2
[a     b] [c     d] = relocation required (b ≠ c)

   b1        b2
[a     b] [b     c] = no relocation required (b = b)
```


Your task is to design and implement an algorithm that takes a sequence of bookings as input, and returns a permutation that minimises the total number of relocations within the sequence. For example, given

```
   b1         b2        b3        b4
[x     y] [z     x] [y     z] [y     z] = 3 relocations required
```

you could return

```
   b3         b2        b1        b4
[y     z] [z     x] [x     y] [y     z] = 0 relocations required
```

The output sequence must contain the same set of bookings as the input (that is, you can't add or remove any bookings). You cannot change the start or end locations of any bookings. Note that it might not be possible to find a reordered sequence with 0 relocations. Your job is simply to minimise the number as much as possible.

Feel free to use any language/framework you'd like, but make sure it's easy for us to build! 

**When you're done, [Email us](mailto:hr@smove.sg) with either a link to your repo or your zipped solution, including both your source code and your generated output for the given test case.**

### Input Format
A JSON file consisting of an array of booking objects. Each object has an `id`, `start`, and `end`. E.g.:

```
[
	{ "id": 1, "start": 23, "end": 42 },
	
	{ "id": 2, "start": 77, "end": 45},
	
	{ "id": 3, "start": 42, "end": 77 },
	
	. . .
]
```

### Output Format
A JSON file consisting of an array of booking IDs of the reordered sequence. E.g., given the above input:

```
[1, 3, 2]
```

### File
[bookingvalidation.json](bookingvalidation.json)