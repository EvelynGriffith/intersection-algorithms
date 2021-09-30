# Intersection Algorithms

## Evelyn Griffith

## Program Output

### Use eight fenced code blocks to provide output from eight different runs of `intersection` with different inputs

`Summary of the runs for the List-based algorithms:`

`Run 1: ListSingle with a small input`

```
🔬 Here's profiling data from computing an intersection with random data containers of 1000!

  _     ._   __/__   _ _  _  _ _/_   Recorded: 16:23:52  Samples:  1
 /_//_/// /_\ / //_// / //_'/ //     Duration: 0.000     CPU time: 0.000
/   _/                      v4.0.3

Program: intersection --number 1000 --maximum 25 --profile --approach ListSingle

0.001 intersection  intersection\main.py:114
└─ 0.001 compute_intersection_list_single  intersection\main.py:77
```

`Run 2: ListSingle with a large input`

```
🔬 Here's profiling data from computing an intersection with random data containers of 1000000!

  _     ._   __/__   _ _  _  _ _/_   Recorded: 16:35:13  Samples:  1698
 /_//_/// /_\ / //_// / //_'/ //     Duration: 1.826     CPU time: 1.750
/   _/                      v4.0.3

Program: intersection --number 1000000 --maximum 25 --profile --approach ListSingle

1.828 intersection  intersection\main.py:114
├─ 1.800 compute_intersection_list_single  intersection\main.py:77
│  ├─ 1.504 [self]
│  └─ 0.296 list.append  <built-in>:0
│        [2 frames hidden]  <built-in>
└─ 0.029 [self]
```

`Run 1: ListDouble with a small input`

```
🔬 Here's profiling data from computing an intersection with random data containers of 1000!

  _     ._   __/__   _ _  _  _ _/_   Recorded: 16:37:15  Samples:  73
 /_//_/// /_\ / //_// / //_'/ //     Duration: 0.081     CPU time: 0.078
/   _/                      v4.0.3

Program: intersection --number 1000 --maximum 25 --profile --approach ListDouble

0.073 intersection  intersection\main.py:114
├─ 0.072 compute_intersection_list_double  intersection\main.py:61
│  ├─ 0.068 [self]
│  └─ 0.004 list.append  <built-in>:0
│        [2 frames hidden]  <built-in>
└─ 0.001 stop  pyinstrument\profiler.py:136
      [3 frames hidden]  pyinstrument
```

`Run 2: ListDouble with a large input`

```
🔬 Here's profiling data from computing an intersection with random data containers of 10000!

  _     ._   __/__   _ _  _  _ _/_   Recorded: 16:47:43  Samples:  8973
 /_//_/// /_\ / //_// / //_'/ //     Duration: 9.321     CPU time: 8.969
/   _/                      v4.0.3

Program: intersection --number 10000 --maximum 25 --profile --approach ListDouble

9.311 intersection  intersection\main.py:114
└─ 9.311 compute_intersection_list_double  intersection\main.py:61
   ├─ 8.495 [self]
   └─ 0.816 list.append  <built-in>:0
         [2 frames hidden]  <built-in>
```

`Run 1: TupleSingle with a small input`

```
🔬 Here's profiling data from computing an intersection with random data containers of 1000!

  _     ._   __/__   _ _  _  _ _/_   Recorded: 16:50:32  Samples:  1
 /_//_/// /_\ / //_// / //_'/ //     Duration: 0.010     CPU time: 0.016
/   _/                      v4.0.3

Program: intersection --number 1000 --maximum 25 --profile --approach TupleSingle

0.008 intersection  intersection\main.py:114
└─ 0.008 compute_intersection_tuple_single  intersection\main.py:103
```

`Run 2: TupleSingle with a large input`

```
🔬 Here's profiling data from computing an intersection with random data containers of 10000!

  _     ._   __/__   _ _  _  _ _/_   Recorded: 17:02:17  Samples:  1
 /_//_/// /_\ / //_// / //_'/ //     Duration: 0.139     CPU time: 0.141
/   _/                      v4.0.3

Program: intersection --number 10000 --maximum 25 --profile --approach TupleSingle

0.144 intersection  intersection\main.py:114
└─ 0.144 compute_intersection_tuple_single  intersection\main.py:103
```

`Run 1: TupleDouble with a small input`

```
🔬 Here's profiling data from computing an intersection with random data containers of 1000!

  _     ._   __/__   _ _  _  _ _/_   Recorded: 17:05:17  Samples:  1
 /_//_/// /_\ / //_// / //_'/ //     Duration: 5.105     CPU time: 5.031
/   _/                      v4.0.3

Program: intersection --number 1000 --maximum 25 --profile --approach TupleDouble

5.095 intersection  intersection\main.py:114
└─ 5.095 compute_intersection_tuple_double  intersection\main.py:91
```

`Run 2: TupleDouble with a large input`

```

TODO: Whenever possible, please use the same "small" and "large" inputs for both
the List-based and Tuple-based algorithms.

TODO: Do not run the program with the `--display` option when conducting
experiments!

TODO: Document and justify your choice for the `number` and `maximum` variables.

#### Two outputs from running the `ListSingle` algorithm with different inputs

#### Two outputs from running the `ListDouble` algorithm with different inputs

#### Two outputs from running the `TupleSingle` algorithm with different inputs

#### Two outputs from running the `TupleDouble` algorithm with different inputs

## Performance Analysis

TODO: Provide three paragraphs that explain which algorithm is fastest, by how
much it is faster, and how you knew that the it was faster, referencing the data
in the aforementioned command outputs to support your response. You should make
sure that you answer the following research questions:

- RQ: Is intersection faster with a list or a tuple?
- RQ: Is intersection faster with a double-for-loop or a single-for-loop?
- RQ: Overall, what is the fastest approach for computing the intersection?

TODO: Make sure that your responses explain WHY certain algorithms are faster!
TODO: It is not sufficient to only explain WHICH algorithm is faster!

## Source Code

### Describe in detail how the completed source code works

#### A class that defines the four algorithmic options for running the experiment

TODO: Use a fenced code block to provide the requested source code
TODO: Write at least one paragraph to explain the request source code

#### A function signature that defines the command-line interface for `intersection`

TODO: Use a fenced code block to provide the requested source code
TODO: Write at least one paragraph to explain the request source code
TODO: Explain each of the command-line arguments for this program

#### A function that can generate a data container with random values in it

TODO: Use a fenced code block to provide the requested source code
TODO: Write at least one paragraph to explain the request source code
TODO: Explain each line of source code in this function

### What was the greatest challenge that you faced when completing this assignment?

TODO: Provide a one-paragraph response that answers this question in your own words.

### Leveraging your response to the previous question, how did you overcome the challenge?

TODO: Provide a one-paragraph response that answers this question in your own words.
